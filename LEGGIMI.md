# Sfere Magiche – versione desktop (Windows e Linux)

Richiede **Node.js 18+** (https://nodejs.org). Il gioco funziona offline.

## Provarlo subito
- Windows: doppio clic su `avvia.bat`
- Linux: `./avvia.sh`
- In alternativa: `npm install` poi `npm start`

## Creare l'installer
Esegui il comando sul sistema di destinazione (consigliato):

| Sistema | Comando | Risultato in `dist/` |
|---|---|---|
| Windows | `npm install` poi `npm run dist:win` | `Sfere Magiche Setup 1.0.0.exe` (installer) e versione portable `.exe` |
| Linux | `npm install` poi `npm run dist:linux` | `.AppImage`, `.rpm` (Fedora: `sudo dnf install ./file.rpm`) e `.deb` (Debian/Ubuntu) |

Su Linux l'AppImage va resa eseguibile: `chmod +x Sfere*.AppImage`.

### Build automatica (opzionale)
Carica la cartella su GitHub: il workflow `.github/workflows/build.yml` crea
sia l'installer Windows sia i pacchetti Linux e li rende scaricabili.

## Note
- Utenti e record sono salvati sul PC dell'utente (nel profilo dell'app) e restano dopo la chiusura.
- `F11` = schermo intero. Nel menu utenti c'è il pulsante "Chiudi applicazione".
- Per cambiare l'icona sostituisci `build/icon.png` (512×512).

## Tutto da GitHub (senza terminale)
Carica i file dal sito, poi crea a mano `.github/workflows/build.yml` incollando il contenuto di `COPIA-workflow-build.yml`. Gli installer compaiono in Actions > Artifacts.
