# Solare Italiano — Ideazione Contenuti Social

Sistema di ideazione contenuti reel Instagram per **SOLARE ITALIANO**, azienda italiana che installa e fa manutenzione di impianti per riscaldamento, raffrescamento ed energia rinnovabile.

**Logica**: Tu + Claude generi le idee → i venditori validano via WhatsApp → l'agenzia produce i video.

```
Social/
├── CLAUDE.md                    ← questo file (istruzioni complete)
├── 01_Tracker/
│   └── Solare_Italiano_Content_System.xlsx   ← fonte di verità locale
├── 02_Generazione_Idee/         ← idee generate (YYYY-MM-DD_tipo.md)
└── 03_Brief_Agenzia/            ← brief 60-90 sec per l'agenzia
```

**Flusso rapido**:
1. Lunedì mattina → genera idee → atterrano in `02_Generazione_Idee/` e nel Master Idee
2. Martedì → manda messaggio WhatsApp ai venditori (SÌ/NO/FORSE)
3. Mercoledì sera → aggiorna Stato nel Master (Shortlist / Scartata / Nuova)
4. Ultimo venerdì del mese → brief per l'agenzia in `03_Brief_Agenzia/`
5. Prima settimana del mese → audit gap mensile

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

**Master Idee** = unica fonte di verità. Scrivi solo qui (mai in Shortlist o Libreria — sono viste FILTER auto-aggiornate).

| # | Colonna | Note |
|---|---|---|
| 1 | Data inserimento | data reale |
| 2 | Fonte | Ispirazione / Notizie / Ideazione Claude / Scheduled Task / Agenzia / Topic mese |
| 3 | Titolo Reel | una riga |
| 4 | Pain | problema del cliente (1 frase) |
| 5 | Breve descrizione | cosa mostra/dice il reel (1-2 righe) |
| 6 | Categoria Contenuto | dalla tassonomia sopra |
| 7 | Angolo | dalla tassonomia sopra, coerente con la categoria |
| 8 | Note | annotazioni libere |
| 9 | Stato | Nuova / Shortlist / Scartata / Postata |
| 10 | Priorità (1-5) | la mette l'utente, non Claude |
| 11 | Mese Creazione Contenuti | nome italiano (Gennaio, Febbraio, …) |
| 12–18 | Post-pubblicazione | Data pub / Link / Views / Like / Salvati / Commenti / Lead |

**Shortlist Mensile** = FILTER auto (Stato=Shortlist + mese corrente). Non modificare a mano.
**Libreria Contenuti** = FILTER auto (Stato=Postata). Non modificare a mano.

### Leggere e scrivere l'xlsx da Claude Code

Prerequisito: `pip3 install openpyxl -q`

Attenzione: se Excel ha il file aperto, trovi `~$Solare_Italiano_Content_System.xlsx` nella stessa cartella — chiudi Excel prima di scrivere.

**Leggere il Master Idee:**
```python
import openpyxl
wb = openpyxl.load_workbook(
    '/Users/daviderossetto/AI/Solare_Italiano/Social/01_Tracker/Solare_Italiano_Content_System.xlsx',
    data_only=True
)
ws = wb['Master Idee']
rows = list(ws.iter_rows(values_only=True))
header, data = rows[0], rows[1:]
```

**Aggiungere righe al Master Idee:**
```python
import openpyxl
from datetime import date
from openpyxl.styles import Border, Side, Alignment

thin = Side(border_style="thin", color="BFBFBF")
border = Border(left=thin, right=thin, top=thin, bottom=thin)
center = Alignment(horizontal="center", vertical="center", wrap_text=True)
left_wrap = Alignment(horizontal="left", vertical="center", wrap_text=True)
MESI = ["Gennaio","Febbraio","Marzo","Aprile","Maggio","Giugno",
        "Luglio","Agosto","Settembre","Ottobre","Novembre","Dicembre"]

wb = openpyxl.load_workbook(
    '/Users/daviderossetto/AI/Solare_Italiano/Social/01_Tracker/Solare_Italiano_Content_System.xlsx'
)
ws = wb['Master Idee']
oggi = date.today()
mese = MESI[oggi.month - 1]

first_empty = 4
while ws.cell(row=first_empty, column=3).value is not None:
    first_empty += 1

# ideas = [(titolo, pain, descrizione, categoria, angolo), ...]
for i, (titolo, pain, descr, cat, ang) in enumerate(ideas):
    r = first_empty + i
    values = [oggi, "Scheduled Task", titolo, pain, descr, cat, ang,
              "Generato automaticamente di notte", "Nuova", None, mese,
              None, None, None, None, None, None, None]
    for c, v in enumerate(values, start=1):
        cell = ws.cell(row=r, column=c, value=v)
        cell.border = border
        cell.alignment = left_wrap if c in (3, 4, 5, 8, 13) else center
        if c == 1:
            cell.number_format = "dd/mm/yyyy"

wb.save('/Users/daviderossetto/AI/Solare_Italiano/Social/01_Tracker/Solare_Italiano_Content_System.xlsx')
```

---

## Automazione attiva

### Agente notturno (ogni notte alle 03:00 ora italiana)

Genera 3–5 nuove idee → le aggiunge al Master Idee (`Stato = "Nuova"`, `Fonte = "Scheduled Task"`) → salva copia `.md` in `02_Generazione_Idee/`. Visibile su: https://claude.ai/code/routines

**Nota**: per leggere/scrivere il tracker xlsx l'agente remoto ha bisogno che il progetto sia su un repository GitHub (altrimenti i file locali non sono accessibili in cloud). Senza repo, l'agente lavora solo su Google Drive.

### Agente mid-month (15 di ogni mese alle 03:00 ora italiana)

Legge il foglio "Shortlist Mensile" dal tracker xlsx → crea il file "Shortlist [Mese] [Anno] — Solare Italiano" su Google Drive (cartella "10 Social Media"). I file dei mesi precedenti rimangono su Drive come storico. Visibile su: https://claude.ai/code/routines

### Google Drive

- Cartella "10 Social Media": ID `1nd5F1dC53st4iTcyVD6XH_lR0Uh-riaD`
- MCP connesso: `mcp__claude_ai_Google_Drive__*`
- Shortlist Maggio 2026: ID `1sEIHHSfeEtsp1uCf_GgRfGHAtgzV7nrCc_PYFndV9pw`

---

## Stile output

- Sempre in italiano
- Linguaggio semplice, zero gergo tecnico
- Concreto (esempi, casi reali) ma senza conti numerici di risparmio
- Diretto, senza disclaimer e premesse lunghe
