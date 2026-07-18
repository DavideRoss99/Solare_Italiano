# Solare Italiano — Ideazione Contenuti Social

Sistema di ideazione contenuti reel Instagram per **SOLARE ITALIANO**, azienda italiana che installa e fa manutenzione di impianti per riscaldamento, raffrescamento ed energia rinnovabile.

**Logica**: Tu + Claude generi le idee → i venditori validano via WhatsApp → l'agenzia produce i video.

```
Social/
├── CLAUDE.md                    ← questo file (istruzioni complete)
├── 01_Tracker/
│   └── Solare_Italiano_Content_System.xlsx   ← fonte di verità locale
├── 03_Brief_Agenzia/            ← brief 60-90 sec per l'agenzia
└── 04_News_Feed/                ← news brief giornalieri (agente notturno), news_YYYY-MM-DD.md
```

**Flusso mensile**:
1. Ogni notte → agente cerca news rilevanti sul web, scrive un news brief, genera MASSIMO 5 idee di qualità (anche meno) → Master Idee (Stato=Nuova)
2. Tu segni le idee migliori come Stato=Shortlist (e quelle scartate come Stato=Scartata) nel tracker
3. 1° del mese → agente crea Google Sheet "Shortlist — Solare Italiano — [Mese] [Anno]" su Drive + rimuove da Master Idee + sposta le Scartata in Cimitero Idee
4. Prime 2 settimane → meeting interno per decidere: Confermata / Posticipata / Scartata (nel Google Sheet)
5. 15° del mese → agente legge il Google Sheet DI QUESTO MESE (cerca il titolo esatto con mese/anno corrente) e riporta nel Master Idee (Confermata→Produzione, Posticipata→Nuova, Scartata→Cimitero Idee)
6. 28° del mese → agente archivia le idee con Stato=Produzione in Libreria Contenuti

---

## Contesto azienda

- Sito: https://www.solareitaliano.it/ — IG: https://www.instagram.com/solare_italiano_srl
- Email operativa: solareitalianosrl@gmail.com
- Mix prodotti per priorità strategica:
  1. RISCALDAMENTO LEGNA/PELLET (stufe, inserti, camini, cucine economiche, termostufe, termocamini, termocucine — prodotto principale)
  2. POMPA DI CALORE (in crescita, spingere di più)
  3. SOLARE (termico + fotovoltaico + accumulo)
  4. CLIMATIZZATORI
  5. MOBILITÀ ELETTRICA (colonnine di ricarica)
- Marketing video: gestito da agenzia esterna. Solare Italiano gestisce l'ideazione.

**Target audience**: proprietari di casa italiani, 40–65 anni. Non tecnici. Confusi su differenze tra prodotti e incentivi. Motivati da risparmio e benefici fiscali.

**Pilastro contenuti**: Reel Instagram da 60–90 secondi. Persone che parlano in modo semplice. Spiegare cose complesse a non esperti.

---

## Regole non negoziabili

### Regola d'oro
> *Un proprietario di casa di 55 anni, confuso su Conto Termico o sulle differenze tra caldaie, **salverebbe** questo video?*

Se no → scarta. Non proporre nemmeno ai venditori.

### Regole di esclusione

| Argomento | Perché no |
|---|---|
| Prezzo del pellet, andamento mercato, prestagionale, "quando comprare i sacchi" | Solare Italiano vende stufe/caldaie, NON il pellet come combustibile |
| Calcoli numerici di risparmio (€/MWh, "risparmi X€ l'anno", tabelle gas vs pellet con cifre) | Posizione aziendale: angolo risparmio qualitativo sì, cifre esplicite no |
| Promesse esagerate ("risparmi del 70%!") | Brand safety + nessuna fonte verificabile |
| Tecnicismi da ingegnere (COP, SCOP, PCI ecc. senza spiegazione) | Target non tecnico |
| Tono corporate aziendale | Format reel chiede tono umano |
| Contenuti senza utilità pratica | Falliscono la regola d'oro |

---

## Tassonomia contenuti (fonte: foglio Tech del tracker)

### Catalogo prodotti

| Famiglia | Prodotto | Categoria tracker |
|---|---|---|
| Riscaldamento legna/pellet | Stufe | Prodotto - Stufe |
| Riscaldamento legna/pellet | Inserti e Camini | Prodotto - Inserti e Camini |
| Riscaldamento legna/pellet | Cucine economiche | Prodotto - Cucine economiche |
| Riscaldamento legna/pellet | Termostufe | Prodotto - Termostufe |
| Riscaldamento legna/pellet | Termocamini | Prodotto - Termocamini |
| Riscaldamento legna/pellet | Termocucine | Prodotto - Termocucine |
| Caldaia centralizzata | Caldaie | Prodotto - Caldaie |
| Riscaldamento/Raffrescamento | Pompe di Calore | Prodotto - Pompe di Calore |
| Raffrescamento | Climatizzatore | Prodotto - Climatizzatore |
| Solare | Pannelli Solari | Prodotto - Pannelli Solari |
| Solare | Pannelli Fotovoltaici | Prodotto - Pannelli Fotovoltaici |
| Solare | Batterie di Accumulo | Prodotto - Batterie di Accumulo |
| Mobilità elettrica | Colonnine di Ricarica | Prodotto - Colonnine di Ricarica |
| Trasversale | — | FAQ |
| Trasversale | — | Conosci Solare Italiano |
| Trasversale | — | Lavori |

### Angoli consentiti per categoria

**Tutte le categorie Prodotto** (Stufe, Inserti e Camini, Cucine economiche, Termostufe, Termocamini, Termocucine, Caldaie, Pompe di Calore, Climatizzatore, Pannelli Solari, Pannelli Fotovoltaici, Batterie di Accumulo, Colonnine di Ricarica):
> Come funziona / A cosa viene sostituito / Quando sostituirlo / Come scegliere il modello giusto / Dove si può installare / Manutenzione / Incentivi / Errore comune / Confronto con alternative

**FAQ**:
> Domanda burocratica / normativa / Domanda economica / Paura / Scetticismo / Confronto tra prodotti / Curiosità generale

**Conosci Solare Italiano**:
> Servizi offerti / Corsi di sicurezza / Certificazioni / Storia / Valori / Team / Sedi / Zone operative / Garanzie / Assistenza post-vendita

**Lavori**:
> Prima / Dopo installazione / Sopralluogo / Cantiere in corso / Caso reale cliente / Time-lapse installazione / Dietro le quinte squadra

### Lista completa angoli (tutti)
A cosa viene sostituito · Cantiere in corso · Caso reale cliente · Certificazioni · Come funziona · Come scegliere il modello giusto · Confronto con alternative · Confronto tra prodotti · Corsi di sicurezza · Curiosità generale · Dietro le quinte squadra · Domanda burocratica / normativa · Domanda economica · Dove si può installare · Errore comune · Garanzie / Assistenza post-vendita · Incentivi · Manutenzione · Paura / Scetticismo · Prima / Dopo installazione · Quando sostituirlo · Sedi / Zone operative · Servizi offerti · Sopralluogo · Storia / Valori · Team · Time-lapse installazione

---

## Come generare buone idee

### Framework di ideazione

Ogni buona idea nasce da un **pain specifico del cliente** + un **prodotto concreto** + un **angolo che risolve il pain**. Non partire mai dal prodotto in astratto — parti dal dubbio, dalla paura o dall'errore che il cliente fa.

**Formula**: [Pain del cliente] + [Prodotto] + [Angolo] = Idea reel

**Pain ricorrenti per famiglia di prodotto**:

| Famiglia | Pain tipici |
|---|---|
| Stufe / Inserti / Camini | "Il camino disperde tutto il calore", "non so quale inserto scegliere", "la stufa fa fumo — non funziona" |
| Cucine economiche | "È roba da baita vintage, non è per case moderne", "non so che differenza c'è con la stufa normale" |
| Termostufe / Termocamini / Termocucine | "Non sapevo che scalda anche i termosifoni", "pensavo servissero tre impianti separati" |
| Caldaie | "La mia caldaia ha 15 anni, non so quando cambiarla", "quale incentivo prendo?" |
| Pompe di Calore | "Funziona davvero al freddo?", "è solo per case nuove?", "spendo di più in corrente?" |
| Climatizzatori | "Lo uso solo d'estate — peccato buttarlo via d'inverno" |
| Pannelli Solari / Fotovoltaici | "Non capisco la differenza tra termico e fotovoltaico" |
| Batterie di Accumulo | "I pannelli producono di giorno quando non sono a casa — si perde tutto?" |
| Colonnine di Ricarica | "Ho l'auto elettrica e carico sulla presa normale — basta no?" |
| Incentivi (FAQ) | "Ho paura di perdere l'Ecobonus", "non so se mi spetta il Conto Termico" |

**Mix prodotti da mantenere ogni settimana**: almeno 1 Pompa di Calore, 1 riscaldamento legna/pellet (prodotto, non combustibile), 1 incentivo/FAQ. Non fare settimane mono-prodotto.

**Target mensile**: Riscaldamento legna/pellet ~35% / Pompa di Calore ~30% / Solare ~15% / Climatizzazione ~10% / Generale/Incentivi/Team ~10%

### Esempi buoni vs scartati

**Buoni** (passano la regola d'oro):
- "La pompa di calore funziona a -10°C?" — Pain: paura del freddo — PdC · Come funziona
- "Stufa a pellet fa fumo? Ecco i 2 errori più comuni" — Pain: pensa sia rotta, è uso sbagliato — Stufe · Errore comune
- "Camino aperto: dove va a finire il calore?" — Pain: il camino è bello ma disperde — Inserti e Camini · A cosa viene sostituito
- "Conto Termico 2026: chi può richiederlo?" — Pain: confusione su chi ha diritto — FAQ · Incentivi
- "Termocucina: cuoci, scaldi i termosifoni e fai l'acqua calda" — Pain: non sa che esiste — Termocucine · Come funziona

**Scartati** (falliscono regola d'oro):
- "Il pellet quest'anno conviene comprarlo a ottobre" → ESCLUSO (prezzo pellet-combustibile)
- "Con la PdC risparmi €600 l'anno rispetto al gas" → ESCLUSO (cifra numerica di risparmio)
- "Il COP della nostra PdC è 4.8" → ESCLUSO (tecnicismo senza spiegazione)
- "Solare Italiano: leader nel settore da 20 anni" → ESCLUSO (corporate, nessuna utilità per chi guarda)

### Varia gli angoli per lo stesso prodotto

Per le Pompe di Calore puoi fare settimane diverse su: Come funziona → Errore comune → Incentivi → Dove si può installare → Confronto con alternative. Non ripetere lo stesso angolo due volte di fila sullo stesso prodotto.

---

## Architettura tracker xlsx

Tre sheet separati, stesse 10 colonne ciascuno. I dati si **spostano** (non si copiano) da uno sheet all'altro.

| # | Colonna | Note |
|---|---|---|
| 1 | Data | generazione in Master; produzione in Libreria |
| 2 | Fonte | Ideazione Claude / Scheduled Task / Agenzia / Topic mese |
| 3 | Titolo Reel | una riga |
| 4 | Pain | problema del cliente (1 frase) |
| 5 | Breve descrizione | cosa mostra/dice il reel (1-2 righe) |
| 6 | Categoria Contenuto | dalla tassonomia |
| 7 | Angolo | dalla tassonomia, coerente con categoria |
| 8 | Note | annotazioni libere |
| 9 | Stato | vedi sotto per valori validi per sheet |
| 10 | Priorità | la mette l'utente, non Claude |

**Master Idee** — idee generate. Stato validi: `Nuova` (default) / `Scartata` / `Shortlist` (impostato dall'utente) / `Produzione` (impostato dall'agente del 15°). Dati da row 4.

**Libreria Contenuti** — contenuti prodotti. Data = data produzione. Popolato dalla routine del 28°.

**Cimitero Idee** — idee scartate (Stato=Scartata), archiviate per riferimento invece di essere cancellate. Popolato dalla routine del 1° (scartate segnate direttamente in Master) e dalla routine del 15° (scartate decise nel Google Sheet mensile). Stessa struttura a 10 colonne.

### Leggere e scrivere l'xlsx da Claude Code

Prerequisito: `pip3 install openpyxl -q`

Attenzione: se Excel ha il file aperto, trovi `~$Solare_Italiano_Content_System.xlsx` — chiudi Excel prima di scrivere.

**Aggiungere righe al Master Idee:**
```python
import openpyxl
from datetime import date
from openpyxl.styles import Border, Side, Alignment

XLSX = '/Users/daviderossetto/AI/Solare_Italiano/Social/01_Tracker/Solare_Italiano_Content_System.xlsx'
thin = Side(border_style="thin", color="BFBFBF")
border = Border(left=thin, right=thin, top=thin, bottom=thin)
center = Alignment(horizontal="center", vertical="center", wrap_text=True)
left_wrap = Alignment(horizontal="left", vertical="center", wrap_text=True)

wb = openpyxl.load_workbook(XLSX)
ws = wb['Master Idee']

first_empty = 4
while ws.cell(row=first_empty, column=3).value is not None:
    first_empty += 1

# ideas = [(titolo, pain, descrizione, categoria, angolo), ...]
for i, (titolo, pain, descr, cat, ang) in enumerate(ideas):
    r = first_empty + i
    values = [date.today(), "Scheduled Task", titolo, pain, descr, cat, ang,
              "Generato automaticamente di notte", "Nuova", None]
    for c, v in enumerate(values, start=1):
        cell = ws.cell(row=r, column=c, value=v)
        cell.border = border
        cell.alignment = left_wrap if c in (3, 4, 5, 8) else center
        if c == 1:
            cell.number_format = "dd/mm/yyyy"

wb.save(XLSX)
```

**Spostare righe tra sheet (pattern generico):**
```python
# Leggi righe da sorgente
source_rows = []
source_row_nums = []
for r in range(4, 500):
    if ws_src.cell(r, 3).value is None:
        break
    if ws_src.cell(r, 9).value == 'Shortlist':  # o altro Stato
        source_rows.append([ws_src.cell(r, c).value for c in range(1, 11)])
        source_row_nums.append(r)

# Aggiungi a destinazione
first_empty_dst = 4
while ws_dst.cell(first_empty_dst, 3).value is not None:
    first_empty_dst += 1
for i, row in enumerate(source_rows):
    r = first_empty_dst + i
    for c, v in enumerate(row, 1):
        cell = ws_dst.cell(r, c, v)
        cell.border = border
        cell.alignment = left_wrap if c in (3, 4, 5, 8) else center
        if c == 1: cell.number_format = "dd/mm/yyyy"

# Elimina da sorgente (dal basso verso l'alto)
for r in reversed(source_row_nums):
    ws_src.delete_rows(r)
```

---

## Automazione attiva

**2026-07-18: fix di un bug di duplicazione** — l'agente del 15° rileggeva un vecchio file Drive già processato (il tool `mcp__Google_Drive__create_file` NON sovrascrive un file esistente con lo stesso titolo, crea sempre un file nuovo), causando righe duplicate ripetute nel Master Idee. Fix: ogni ciclo mensile ora usa un titolo Drive univoco con mese+anno (`Shortlist — Solare Italiano — Luglio 2026`), quindi l'agente del 15° cerca SOLO il file del mese corrente e non può mai rileggere decisioni di un mese precedente. Vedi [[feedback_collaboration]] per il perché di questo design.

### Agente notturno (ogni notte alle 03:00 ora italiana)
ID: `trig_01K2HvLvGgo6b8nZS9CMb4Sp`

1. Cerca su web (tool WebSearch) notizie recenti (7-14gg) su incentivi/normativa energetica rilevanti → scrive news brief in `Social/04_News_Feed/news_YYYY-MM-DD.md`
2. Genera MASSIMO 5 idee di qualità (anche meno se il materiale non basta — qualità prima di quantità) → aggiunge al **Master Idee** (`Stato=Nuova`, `Fonte=Scheduled Task`)
3. Push xlsx + news brief su GitHub

### Agente shortlist — 1° del mese (alle 03:00 ora italiana)
ID: `trig_015amyZi8gBy1fDeD9jfo2ts`

1. Legge idee con `Stato=Shortlist` da Master Idee → crea **Google Sheet "Shortlist — Solare Italiano — [Mese] [Anno]"** su Drive (nuovo file ogni mese, mai sovrascritto) → appende a Shortlist Mensile (senza cancellare righe di mesi precedenti non ancora risolte) → rimuove dal Master Idee
2. Legge idee con `Stato=Scartata` da Master Idee → sposta in **Cimitero Idee** → rimuove dal Master Idee
3. Push xlsx su GitHub

### Agente shortlist — 15° del mese (alle 03:00 ora italiana)
ID: `trig_01APWUXWKgfUBREgND8wfmMw`

Cerca ESATTAMENTE il file Drive del mese corrente (`Shortlist — Solare Italiano — [Mese corrente] [Anno]`) → processa le idee in base allo Stato impostato dall'utente:
- `Confermata` → Master Idee con `Stato=Produzione`
- `Posticipata` → Master Idee con `Stato=Nuova`
- `Scartata` → **Cimitero Idee** (NON eliminata, archiviata)
- Vuoto/`Shortlist` → non processata ancora
Se il file del mese corrente non esiste, esce senza fare nulla (non cerca file di mesi diversi).

### Agente archivio — 28° del mese (alle 03:00 ora italiana)
ID: `trig_01QzkATpaExJiTHBfXmMCym3`

Legge idee con `Stato=Produzione` da Master Idee → sposta in **Libreria Contenuti** (Data = oggi) → upload xlsx su GitHub.

### Google Drive

- Cartella "10 Social Media": ID `1nd5F1dC53st4iTcyVD6XH_lR0Uh-riaD`
- MCP connesso: `mcp__claude_ai_Google_Drive__*` — **non ha un tool di delete/rename**, solo create/search/read. Per questo lo schema usa un titolo univoco per mese invece di provare a sovrascrivere.
- File shortlist di un mese: `Shortlist — Solare Italiano — [Mese] [Anno]` (es. "Luglio 2026") — cercare per titolo ESATTO, non per "il più recente"
- File orfani da ripulire manualmente (pre-fix, titolo senza mese, ignorare/cancellare da Drive): `1ZZLgLyaP0sYDLQO9x5ypmZLdM-OhH_BoyKyTWq97HTo` (stale da giugno) e `1NUr3Sj7e3ynBhn_Btmm3YQNBlIDMyfFI3y-ZNRikkKU` (creato per errore il 18/07 prima del fix naming)
- Shortlist Luglio 2026 (corrente): ID `1V_0nAFjnD_GBilizig7p9bOGPq1aunEDnyUxoGqI1GU`

### Nota sicurezza: PAT GitHub nei trigger
Le routine push-su-GitHub usano un Personal Access Token. Non è possibile aggiornare il prompt di un trigger via tool se contiene il PAT in chiaro (bloccato da classificatore di sicurezza automatico) — bisogna editarlo a mano su claude.ai/code/routines. I trigger 1° e 15° del mese hanno attualmente il placeholder `INSERISCI_QUI_IL_TUO_GITHUB_PAT` al posto del token reale nello step di push: va sostituito manualmente prima del prossimo ciclo (1° agosto), altrimenti lo step di push xlsx su GitHub fallisce silenziosamente (il resto della routine — Drive, xlsx locale — funziona comunque).

---

## Stile output

- Sempre in italiano
- Linguaggio semplice, zero gergo tecnico
- Concreto (esempi, casi reali) ma senza conti numerici di risparmio
- Diretto, senza disclaimer e premesse lunghe
