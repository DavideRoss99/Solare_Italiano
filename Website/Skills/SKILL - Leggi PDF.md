# SKILL — Leggi PDF in modo efficiente

## Obiettivo
Leggere documenti PDF tecnici (listini, schede, certificazioni) estraendo solo le informazioni necessarie, senza consumare token inutili.

---

## Strategia di lettura (in ordine)

### 1. Prima lettura — scansione rapida
Leggi sempre solo le prime pagine del PDF:
```
Read(file_path="...", pages="1-2")
```
Le specifiche tecniche nei listini di prodotto si trovano quasi sempre nella prima o seconda pagina.

### 2. Verifica del contenuto
Dopo la Read, controlla che il risultato contenga testo reale (non solo il messaggio di sistema "PDF file read successfully"). Se il testo è vuoto o solo metadati, riprova con un range più ampio: `pages: "1-3"`.

### 3. Lettura mirata
Se le informazioni sono su pagine specifiche (es. tabella tecnica a pag. 3, dimensioni a pag. 4):
```
Read(file_path="...", pages="3-4")
```
Non leggere mai l'intero PDF se non strettamente necessario.

### 4. Regola del "già letto"
Se una pagina è già stata letta in questa sessione, **non rileggerla**. Estrai i dati dal contesto già presente.

---

## Struttura tipica dei PDF di prodotto (Solare Italiano)

| Posizione | Contenuto tipico |
|---|---|
| Pagina 1 | Nome modello, foto, claims principali |
| Pagina 2–3 | Tabella specifiche tecniche (potenza, dimensioni, rendimento) |
| Ultima pagina | Certificazioni, codici prodotto |

---

## Dati da estrarre dai PDF

Per ogni prodotto, cerca:
- **Potenza nominale** (kW) — cerca "kW", "potenza nominale", "nominal power"
- **Rendimento** (%) — cerca "rendimento", "efficiency", "η"
- **Dimensioni** B×H×P (mm) — cerca tabella dimensioni
- **Peso** (kg)
- **Scarico fumi** (Ø mm + posizione)
- **Certificazioni** — cercare loghi/testo: Ecodesign, D.M. 186, CE, A+
- **Classe energetica** — cercare "A+", "A++", "A+++"
- **Riscaldamento max** (m²) — non sempre presente; se assente → `n.d.`

---

## Formati valore
- Dati non trovati → `n.d.`
- Dati stimati o non da fonte ufficiale → aggiungere `(*)`
- Non inventare mai dati non presenti nel PDF

---

## File PDF disponibili
Cartella: `Website/Listini/`

I file sono nominati come: `{Marchio} {NomeProdotto}.pdf`

---

## Note operative
- I PDF in `Listini/` sono listini tecnici originali dei produttori — usarli come fonte primaria
- Se un dato è assente nel PDF, integrare dal sito del produttore (WebFetch) solo come secondo step
- Non leggere mai più di 5 pagine per PDF salvo casi eccezionali
