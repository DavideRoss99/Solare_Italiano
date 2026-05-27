# SKILL — Crea HTML Scheda Prodotto [WIP]

> **Stato:** Work in progress. Il design è definito nel preview, il generatore Python deve essere aggiornato.

## Obiettivo
Generare il file HTML da incollare nella descrizione prodotto di Squarespace Commerce per ogni prodotto del catalogo.

---

## File di riferimento

- **Design di riferimento:** `Website/preview_scheda_prodotto.html`
- **CSS da incollare in Squarespace:** `Website/squarespace_custom.css` *(da aggiornare con la nuova palette)*
- **Dati prodotto:** `Website/0. Scheda Prodotti.xlsx`
- **Dati Conto Termico:** `Website/Conto_Termico.csv`
- **Generatore Python:** `Website/genera_schede_prodotto.py` *(da aggiornare)*

---

## Struttura HTML prodotto

L'HTML segue il design system v2 definito nel preview. Ogni scheda contiene:

```html
<!-- 1. Fuel tag (etichetta combustibile) -->
<span class="si-fuel-tag si-fuel-tag--{tipo}">
  <span class="si-fuel-tag__dot"></span>
  {Combustibile}
</span>

<!-- 2. KPI badges (griglia 2×2) -->
<div class="si-spec-badges">
  <!-- Potenza -->
  <div class="si-badge si-badge--power">...</div>
  <!-- Riscalda (m²) -->
  <div class="si-badge si-badge--area">...</div>
  <!-- Combustibile -->
  <div class="si-badge si-badge--fuel fuel-{tipo}">...</div>
  <!-- Conto Termico — valore Zona F (massimo) dal CSV -->
  <div class="si-badge si-badge--ct">...</div>
</div>

<!-- 3. Descrizione breve -->
<p class="si-description">{Descrizione Corta}</p>

<!-- 4. Accordion specifiche tecniche -->
<details class="si-specs">...</details>

<!-- 5. CTA -->
<a href="/contattaci" class="si-cta">
  Richiedi informazioni
  <svg>...</svg>
</a>
```

---

## Icone SVG per badge (Lucide-style, stroke)

| Badge | Icona | SVG path |
|---|---|---|
| Potenza | Zap | `<polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/>` |
| Riscalda | Home | `<path d="m3 9 9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/>` |
| Legna | Flame | `<path d="M8.5 14.5A2.5 2.5 0 0 0 11 12c0-1.38-.5-2-1-3-1.072-2.143-.224-4.054 2-6 .5 2.5 2 4.9 4 6.5 2 1.6 3 3.5 3 5.5a7 7 0 1 1-14 0c0-1.153.433-2.294 1-3a2.5 2.5 0 0 0 2.5 3z"/>` |
| Pellet | Layers | `<polygon points="12 2 2 7 12 12 22 7 12 2"/><polyline points="2 17 12 22 22 17"/><polyline points="2 12 12 17 22 12"/>` |
| PdC | Wind | `<path d="M17.7 7.7a2.5 2.5 0 1 1 1.8 4.3H2"/><path d="M9.6 4.6A2 2 0 1 1 11 8H2"/><path d="M12.6 19.4A2 2 0 1 0 14 16H2"/>` |
| Conto Termico | Landmark | `<line x1="3" y1="22" x2="21" y2="22"/><line x1="6" y1="18" x2="6" y2="11"/>...` |
| Spec trigger | List | `<line x1="8" y1="6" x2="21" y2="6"/>...` |
| CTA arrow | ArrowRight | `<path d="M5 12h14"/><path d="m12 5 7 7-7 7"/>` |

---

## Palette colori (v2)

```css
--si-accent:       #C4622D;   /* terracotta */
--si-accent-dark:  #A3511F;
--si-text:         #1C1917;   /* charcoal caldo */
--si-muted:        #78716C;
--si-border:       #E7E2DC;
--si-bg:           #F7F5F2;
```

Badge icon backgrounds:
- Potenza: `#FEF3C7` / `#B45309`
- Riscalda: `#DBEAFE` / `#1D4ED8`
- Legna: `#FEF4E6` / `#92400E`
- Pellet: `#FFF7ED` / `#C2410C`
- PdC: `#EEF2FF` / `#3730A3`
- Conto Termico: `#DCFCE7` / `#15803D`

---

## Logica Conto Termico

```python
import csv

def get_ct_zona_f(marchio, prodotto):
    """Restituisce il valore Zona F (massimo) per un prodotto dal CSV."""
    with open('Website/Conto_Termico.csv', newline='', encoding='utf-8') as f:
        for row in csv.DictReader(f):
            if (row['Marchio'].lower() == marchio.lower() and
                    row['Prodotto'].lower() in prodotto.lower()):
                val = row['Zona_F']
                if val:
                    # Formatta come €X.XXX,XX
                    num = float(val)
                    return f"fino a € {num:,.2f}".replace(',', 'X').replace('.', ',').replace('X', '.')
    return '—'
```

---

## TODO prima di usare questo skill

- [ ] Aggiornare `genera_schede_prodotto.py` con il nuovo template HTML (da `preview_scheda_prodotto.html`)
- [ ] Aggiornare `squarespace_custom.css` con la palette v2
- [ ] Validare matching nome prodotto tra Scheda Prodotti e Conto_Termico.csv
- [ ] Testare su 3 prodotti campione prima di generare tutti i 69 prodotti

---

## Output

File generati in: `Website/schede_html/{Marchio}/{Marchio}_{NomeProdotto}.html`

Istruzioni Squarespace:
1. Negozio → seleziona prodotto
2. Descrizione → clicca `<>` (HTML source)
3. Incolla il contenuto del file
4. Salva
