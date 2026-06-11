# Radar AI — repository di stato

Stato persistente del sistema **Radar AI**, un monitor dei trend dell'ecosistema AI
(ricerca + AI engineering) gestito da due Claude Code Routines: una giornaliera e
una settimanale. Questo repo è la memoria del sistema: le routine lo leggono e lo
aggiornano a ogni run.

## Mappa dei file

| Percorso | Contenuto |
|---|---|
| `TRENDS.md` | Il ledger: trend attivi (stadio, confidenza, evidenze), `coda_osservazione`, `rotazione_fonti`, `note_strategia` |
| `ARCHIVE.md` | Trend archiviati, con post-mortem di una riga ciascuno |
| `reports/AAAA-MM-GG.md` | Report giornalieri prodotti dalla routine daily |
| `reports/weekly/AAAA-Wnn.md` | Report settimanali prodotti dalla routine weekly |
| `routines/daily.md` | Copia versionata del prompt della routine daily |
| `routines/weekly.md` | Copia versionata del prompt della routine weekly |
| `docs/` | Materiale di progetto (se presente) |

## Flusso

1. **Daily** — legge `TRENDS.md` e l'ultimo report in `reports/`, raccoglie nuove
   evidenze, aggiorna il ledger (stadi, evidenze, coda di osservazione), scrive
   `reports/AAAA-MM-GG.md` e pusha su `main`.
2. **Weekly** — ricalibra il ledger (promozioni/retrocessioni di stadio,
   archiviazioni in `ARCHIVE.md`, pulizia della coda), aggiorna `note_strategia`
   e scrive `reports/weekly/AAAA-Wnn.md`.

I prompt in `routines/` sono solo la copia versionata: il prompt operativo vive
nella UI delle Routines (claude.ai/code/routines).

## Avvertenza

`TRENDS.md` è scritto da un agente. Ogni modifica manuale va fatta con commit
espliciti (messaggio chiaro, niente edit silenziosi): il prossimo run delle
routine assume che lo stato nel repo sia coerente con la storia dei commit.
