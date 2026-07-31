# 🃏 Burraco Summer Tour — Classifiche

Web app gratuita per gestire le classifiche del torneo di burraco a tappe.
Si apre da **telefono** (per vedere le classifiche) e da **PC** (per aggiornare i punteggi).

## Link pubblico

**https://burraco-summer-tour.github.io/**

Questo link si può condividere con tutti i giocatori (WhatsApp, QR code...). Chi lo apre vede le classifiche in sola lettura: non serve nessuna password.

## Come aggiornare i punteggi (organizzatore)

1. Apri il sito dal **PC**.
2. In fondo, apri **🔐 Area organizzatore** e incolla la tua **chiave** (token GitHub).
3. Crea la nuova **tappa**, poi inserisci i risultati: per ogni coppia scegli i due
   giocatori dall'elenco e digita **MP** (differenza punti) e **VP** (punti classifica).
4. Premi **💾 Salva**: le classifiche si aggiornano da sole e viene creata una copia
   di sicurezza permanente.

### Come creare la chiave (token) — una volta sola

1. Vai su **https://github.com/settings/personal-access-tokens** (Fine-grained tokens).
2. **Generate new token**. Dai un nome (es. *Burraco*), scadenza a piacere.
3. *Resource owner* → scegli l'organizzazione **burraco-summer-tour** (non il tuo account personale).
   Se non compare nell'elenco, abilitala da: pagina dell'organizzazione → Settings →
   *Personal access tokens* → consenti i fine-grained tokens.
4. *Repository access* → **Only select repositories** → scegli **burraco-summer-tour.github.io**.
5. *Permissions* → *Repository permissions* → **Contents** = **Read and write**.
6. **Generate token**, copia la chiave e incollala nell'Area organizzatore dell'app.
   La chiave resta salvata **solo sul tuo dispositivo**.

## Sicurezza dei dati

- Ogni salvataggio è una **versione permanente** su GitHub: si può sempre tornare indietro.
- Dall'app: **Backup JSON** e **Esporta classifiche (CSV)** per avere copie sul tuo PC.
- I dati sono nel file **data.json**.
- La cronologia delle prime 6 tappe è conservata anche nel repository di origine
  (Cyberianna/burraco-summer-tour), da cui l'app è stata spostata il 01/08/2026.

## Struttura

- `index.html` — l'app (tutto qui dentro, nessuna installazione).
- `data.json` — i dati del torneo (giocatori, tappe, risultati).
- `README.md` — questa guida.
