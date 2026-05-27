# SKILL — Trascrivi Conto Termico

## Obiettivo
Leggere le schede Conto Termico (PDF o documenti GSE) relative a nuovi prodotti e aggiungerle al file `Website/Conto_Termico.csv`.

---

## File di riferimento

- **Dati esistenti:** `Website/Conto_Termico.csv`
- **PDF Conto Termico:** `Website/Conto Termico/` — un PDF per marchio (es. `Klover_Conto_Termico.pdf`)
- **PDF listini tecnici:** `Website/Listini/` — schede prodotto dei produttori
- **Excel prodotti:** `Website/0. Scheda Prodotti.xlsx`

### PDF disponibili in `Website/Conto Termico/`
- Famar, Klover, Lacunza, Mitsui, Moretti Design, Ravelli, Rizzoli, Thermorossi

### Marchi ancora da trascrivere
- Nobis, Piazzetta, Jodo, FoxEss, Cerampiù, SPS Istem

---

## Struttura del CSV

```
Marchio,Prodotto,Zona_A,Zona_B,Zona_C,Zona_D,Zona_E,Zona_F
```

- **Zona A–F** = zone climatiche italiane (A = zone miti costiere; F = zone alpine fredde)
- I valori sono importi in €, senza simbolo, con punto decimale (es. `702.46`)
- Zona F = valore massimo (usato nel badge "fino a €X" sulla pagina prodotto)

---

## Come leggere un PDF di Conto Termico

### 1. Identifica il prodotto
Leggi pagina 1 del PDF per trovare:
- Nome esatto del modello
- Marchio
- Potenza (usata per calcolare l'importo)

### 2. Trova la tabella zone climatiche
Cerca nella pagina 1-2 una tabella tipo:

| Zona | Importo (€) |
|------|-------------|
| A    | 702,46      |
| B    | 995,15      |
| ...  | ...         |
| F    | 2.107,38    |

### 3. Estrai i valori
Converti i valori:
- Rimuovi il simbolo € e gli spazi
- Converti la virgola decimale in punto: `1.287,84` → `1287.84`

---

## Come aggiungere al CSV

```python
import csv

nuovi_prodotti = [
    ['Klover', 'Nuovo Modello', '700.00', '990.00', '1280.00', '1630.00', '1980.00', '2096.00'],
]

with open('Website/Conto_Termico.csv', 'a', newline='', encoding='utf-8') as f:
    writer = csv.writer(f)
    writer.writerows(nuovi_prodotti)
```

---

## Verifica deduplicazione

Prima di aggiungere, controlla che il prodotto non esista già:

```python
import csv

with open('Website/Conto_Termico.csv', newline='', encoding='utf-8') as f:
    existing = [(r[0], r[1]) for r in csv.reader(f)]

# Confronta con il nuovo prodotto prima di appendere
```

---

## Nomenclatura prodotti (importante)

Il nome del prodotto nel CSV **deve corrispondere** al nome usato in `0. Scheda Prodotti.xlsx` per permettere il join nel generatore HTML. Se il nome differisce leggermente (es. "Diva Slim" vs "Klover Diva Slim"), usa il nome senza marchio (la colonna `Marchio` lo contiene già).

---

## Prodotti già presenti nel CSV (Maggio 2026)

Nomi prodotti allineati a `0. Scheda Prodotti.xlsx` per il join nel generatore HTML.

| Marchio | Prodotti |
|---|---|
| Lacunza | NIVE 700/800/1000 STAR |
| Famar | Infinity 5S M/XL, Pitagora 30, Kronos 5S, Geysir Kompact (valori Kompact 30), Geysir Wood 5S |
| Rizzoli | ZVI 60, ZVI 80, S 60 Gres, ML 80 Gres |
| Thermorossi | Dorica Evo Wood Metalcolor, Anna EVO6, Agorà EVO6, Margherita EVO6, Violetta EVO6, DORA, Bosky F30 Square EVO5, Lambda S29 – S35 EVO5 (valori S35), Compact S32 GT5 |
| Moretti Design | Ergonomic, Aladino, Kubic, Compact Glass, Monodesign 80, Slot Flat, Slot Vision, Tecnika Exclusive 26 (26kW), Tecnika Glass Short 30 (30kW) |
| Ravelli | Easy 12 |
| Klover | Wave 110, Belvedere 20, Belvedere 22, Diva Slim, Dual (valori legna, max), TKR 27, PFP 160 Glass, Storica KTOP, Altea, Smart 80, Smart 120, Ecompact 35, Ecompact 26 |
| Mitsui Sistem | Multi Flex Trial (3 zone), Multi Flex Quadri (4 zone) |

**Mancanti — nessun PDF CT disponibile:** Nobis, Piazzetta, Jodo, Cerampiù

**Non eleggibili CT:** FoxEss (inverter fotovoltaico + colonnine EV → altri incentivi), SPS Istem (pannelli solari → Conto Energia)
