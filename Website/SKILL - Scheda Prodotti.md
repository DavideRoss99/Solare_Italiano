# SKILL — Raccolta Dati Scheda Prodotti

## Obiettivo
Raccogliere informazioni tecniche e commerciali sui prodotti da schede PDF (cartella Claudio) e/o dal web, e restituirle in formato tabellare Excel.

---

## Fonti da consultare (in ordine di priorità)
1. **PDF nella cartella Claudio** — leggere sempre tutti i file PDF relativi ai prodotti richiesti usando `Read` con `pages: "1-3"`. Verificare che il contenuto effettivo (testo + immagini) sia visibile nel contesto, non solo il messaggio "PDF file read". Se manca il contenuto, rileggere.
2. **Sito web del produttore** — per integrare dimensioni, m³/mq riscaldabili e info assenti nel PDF.
3. **Siti rivenditori** — solo come ultima risorsa.

---

## Struttura della tabella Excel

| # | Colonna | Formato valore | Note |
|---|---|---|---|
| 1 | Categoria Prodotto | Stufe Legna / Stufe Pellet / Stufe Combinato | |
| 2 | Combustione | Legna / Pellet / Pellet + Legna | |
| 3 | Marchio | Es. Nobis | |
| 4 | Nome Prodotto | Nome esatto del modello | |
| 5 | Descrizione Corta | Testo narrativo | Vedi istruzioni sotto |
| 6 | Descrizione Lunga | Testo + bullet • | Vedi istruzioni sotto |
| 7 | Prezzo (€) | Es. `3.150,00` | Solo numero, niente € nel valore |
| 8 | Potenza Nominale (kW) | Es. `9,5` o `4,1 – 10,4` | Solo numero, unità già nel titolo colonna |
| 9 | Riscaldamento max (mq) | Es. `95` o `~85 (~220 m²) (*)` | Solo numero/stima |
| 10 | Serbatoio Pellet (kg) | Es. `35` o `N/A` | Solo numero |
| 11 | Dimensioni B×H×P (mm) | Es. `505 × 1250 × 460` | Aggiungere (*) se stimato |
| 12 | Rendimento (%) | Es. `86,1` | Solo numero, niente % |
| 13 | Classe Energetica | Es. `A+` o `A++` | |
| 14 | Certificazioni | Es. `5★ D.M. 186, Ecodesign 2022, F. Verte 7★` | |
| 15 | PPM (mg/Nm³) | Es. `4,4` o `n.d.` | |
| 16 | Canalizzazione | Descrizione breve | Es. `Posteriore Ø150 (kit opz. +€230)` |
| 17 | Sistema Pulizia | Braciere e vetro | Es. `Braciere autopulente + Clean Glass System` |
| 18 | Wi-Fi | `Sì` / `No` | |
| 19 | Colori | Lista colori | Indicare sovrapprezzi se presenti |
| 20 | Altre Varianti | Modelli correlati | |

---

## Descrizione Corta (Col. 5) — Istruzioni

**Formato: prosa narrativa completa, 150–300 parole.**

Questa colonna contiene il testo principale del prodotto: una descrizione tecnica narrata in modo continuo, senza elenchi. È la versione "lunga in prosa" della scheda.

**Da includere (in prosa, nell'ordine):**
1. Tipo di prodotto (stufa/caldaia/termocamino, combustibile, idro o aria)
2. Potenza nominale, rendimento e superficie riscaldabile
3. Tecnologie distintive rispetto ad altri modelli della gamma (scambiatore, sistema combustione, automazioni)
4. Caratteristiche operative principali: serbatoio, sistema pulizia, canalizzazione, Wi-Fi, optional
5. Finiture/colori e classe energetica

**Stile:**
- Prosa continua — niente bullet, niente elenchi puntati, niente trattini lista
- Tono oggettivo e tecnico, ma leggibile — come una scheda tecnica narrativa
- Lunghezza consigliata: 150–300 parole
- **Vietato:** "Conto Termico", "detrazione fiscale", "incentivi", "risparmio energetico", "green", linguaggio promozionale

---

## Descrizione Lunga (Col. 6) — Istruzioni

**Formato: elenco puntato di specifiche tecniche.**

Questa colonna contiene esclusivamente i dati tecnici del prodotto in forma di bullet list, senza testo narrativo.

**Da includere (ogni voce su riga separata con •):**
- Potenza nominale (kW) — con eventuali varianti (acqua/aria)
- Rendimento (%)
- Riscaldamento max (m² o m³)
- Serbatoio pellet (kg) o N/A
- Consumo combustibile (kg/h)
- Dimensioni B×H×P (mm) o corpo macchina
- Scarico fumi (Ø mm, posizione)
- Peso (kg)
- PPM / emissioni (se disponibile)
- Wi-Fi (Sì/No + eventuali costi)
- Sistema pulizia (braciere + vetro)
- Colori disponibili
- Prezzo (€)
- Certificazioni
- Classe energetica
- Opzionali (con sovrapprezzo se noto)

**Stile:**
- Solo bullet • con valore — nessun testo narrativo, nessuna frase
- Ogni voce: `• Etichetta: valore`
- Dati mancanti → `n.d.`; dati stimati → aggiungere `(*)`
- **Vietato:** prosa, frasi complete, "Conto Termico", linguaggio promozionale

Per **prodotti combinato** (pellet + legna): riportare i dati di entrambe le modalità su righe separate.

---

## Note generali
- Dati non disponibili → `n.d.`
- Dati stimati o non confermati da fonte ufficiale → aggiungere `(*)`
- Per la colonna **Sistema Pulizia** indicare sia il sistema del braciere che del vetro (Clean Glass System)
- Caratteristiche comuni a tutta la gamma → riportarle in sezione separata in fondo alla tabella
