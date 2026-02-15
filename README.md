# 🐧 Gentoo Update Script

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)  
[![Gentoo](https://img.shields.io/badge/Linux-Gentoo-purple?logo=gentoo&logoColor=white)](https://www.gentoo.org/)  
[![Build Status](https://img.shields.io/github/actions/workflow/status/tuo-username/gentooupdate/ci.yml?branch=main&label=build&logo=github)](https://github.com/tuo-username/gentooupdate/actions)  
[![Latest Release](https://img.shields.io/github/v/release/tuo-username/gentooupdate?label=latest%20release&logo=github)](https://github.com/tuo-username/gentooupdate/releases)

Uno script per aggiornare automaticamente **Gentoo Linux** in più fasi, con badge per stato, versione e compatibilità.

---

## ⚡ Panoramica delle Fasi

✅ **Fasi principali dello script:**

- 🔄 **sync** – Sincronizza il portage tree.  
- ⬆️ **update** – Aggiorna il sistema.  
- 🏗 **preservedrebuild** – Ricostruisce pacchetti preservati.  
- 🧹 **depclean** – Rimuove pacchetti non più necessari.  
- 🔧 **revdeprebuild** – Ricostruisce le dipendenze rotte.

---

## 🛠️ Installazione & Utilizzo

Esegui lo script:

```bash
gentooupdate
⚙️ Opzioni disponibili
Opzione	Descrizione
-a true	❗ Interrompe se ci sono notifiche non lette o se emerge è già in esecuzione.
-d "--depclean"	Argomenti passati a revdep-rebuild durante la fase revdeprebuild.
-e ""	Argomenti passati a revdep-rebuild durante la fase revdeprebuild.
-h	Mostra il messaggio di aiuto ed esce.
-n N	Imposta la precisione su N (default 0).
-r "@preserved-rebuild"	Argomenti passati a emerge durante la fase preservedbuild.
-s "--sync"	Argomenti passati a emerge durante la fase sync.
-u "-uDN --with-bdeps=y world"	Argomenti passati a emerge durante la fase update.
💡 Esempi pratici
Aggiornamento standard:

gentooupdate -a false
Aggiornamento avanzato con parametri personalizzati:

gentooupdate -n 20 -u "-uDN --with-bdeps=y --keep-going world"
⚠️ Avvertenze
📌 Leggi eventuali notifiche di emerge prima di procedere.

⚡ Usa -a false per bypassare eventuali blocchi automatici.

👨‍💻 Script destinato a utenti esperti di Gentoo.

📝 Versione & Crediti
Gentoo Update 1.1.1.1

Originale: Nathan Shearer

Editore: Cristian Pozzessere

Licenza: GNU General Public License 3.0

🖌️ Checklist passo passo
🔄 Sincronizzare il portage tree

gentooupdate -s "--sync"
⬆️ Aggiornare il sistema

gentooupdate -u "-uDN --with-bdeps=y world"
🏗 Ricostruire pacchetti preservati

gentooupdate -r "@preserved-rebuild"
🧹 Pulizia pacchetti non necessari

gentooupdate -d "--depclean"
🔧 Ricostruzione dipendenze rotte

gentooupdate -e ""
📊 Badge dinamici consigliati
Puoi aggiornare i badge con il tuo username/repo GitHub:

Build Status:

[![Build Status](https://img.shields.io/github/actions/workflow/status/tuo-username/gentooupdate/ci.yml?branch=main&label=build&logo=github)](https://github.com/tuo-username/gentooupdate/actions)
Ultima release:

[![Latest Release](https://img.shields.io/github/v/release/tuo-username/gentooupdate?label=latest%20release&logo=github)](https://github.com/tuo-username/gentooupdate/releases)
Compatibilità Gentoo:

[![Gentoo](https://img.shields.io/badge/Linux-Gentoo-purple?logo=gentoo&logoColor=white)](https://www.gentoo.org/)
Licenza:

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)
