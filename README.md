# Catalogo offerte Poste per l'app Patrimonio

`catalog.json` contiene le condizioni pubbliche dei prodotti di risparmio postale (buoni fruttiferi, Libretto Smart e depositi Supersmart, polizze Poste Vita) usate dall'app **Patrimonio** per calcolare rendimenti, simulare ritiri anticipati e proporre le offerte più convenienti.

- Contiene **solo dati pubblici dei prodotti**, presi da poste.it, buonielibretti.poste.it, postevita.poste.it e cdp.it. Nessun dato personale.
- L'app lo scarica una volta al giorno da `https://raw.githubusercontent.com/pierolazzaro/patrimonio-catalogo/main/catalog.json` e, se non è raggiungibile, usa la copia inclusa nell'app.
- Viene ricontrollato ogni settimana; `version` e `verified` indicano la data dell'ultima verifica.

I tassi sono annui lordi. Prima di sottoscrivere fa fede il foglio informativo in ufficio postale.

## Campi principali

| Campo | Significato |
|---|---|
| `model` | Regola di calcolo: `libretto`, `conto`, `supersmart`, `bullet` (interessi solo a scadenza), `coeff` (coefficienti di rimborso annuali), `cedola`, `inflazione`, `step` (tassi a scaglioni + premio), `polizza` |
| `rate` | Tasso annuo lordo a scadenza (per le polizze: rendimento retrocesso ipotizzato) |
| `termDays` | Durata in giorni |
| `tax` | Aliquota sugli interessi |
| `eligibility` | Requisiti: `pension`, `inheritance`, `reinvest`, `newMoney` (finestra di nuova liquidità) |
| `deadline` | Ultimo giorno per sottoscrivere, se l'offerta è a tempo |
