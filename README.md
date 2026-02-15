# 🐧 Gentoo Update Script

Uno script per aggiornare automaticamente **Gentoo Linux** in più fasi, progettato per rendere il processo semplice, sicuro e intuitivo.

---

## ⚡ Panoramica delle Fasi

✅ **Fasi principali dello script:**

- 🔄 **sync** – Sincronizza il portage tree.  
- ⬆️ **update** – Aggiorna il sistema.  
- 🏗 **preservedrebuild** – Ricostruisce pacchetti preservati.  
- 🧹 **depclean** – Rimuove pacchetti non più necessari.  
- 🔧 **revdeprebuild** – Ricostruisce le dipendenze rotte.

---

## 🛠️ Utilizzo

Esegui lo script:

```bash
$ gentooupdate
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

$ gentooupdate -a false
Aggiornamento avanzato con parametri personalizzati:

$ gentooupdate -n 20 -u "-uDN --with-bdeps=y --keep-going world"
⚠️ Avvertenze
📌 Leggi eventuali notifiche di emerge prima di procedere.

⚡ Usa -a false per bypassare eventuali blocchi automatici.

👨‍💻 Questo script è destinato a utenti esperti di Gentoo.

🖌️ Checklist passo passo (Mini Manuale Visivo)
🔄 Fase 1 – Sync
# 🔄 Sincronizza il portage tree
$ gentooupdate -s "--sync"
⬆️ Fase 2 – Update
# ⬆️ Aggiorna il sistema con tutti gli aggiornamenti
$ gentooupdate -u "-uDN --with-bdeps=y world"
🏗 Fase 3 – Preserved Rebuild
# 🏗 Ricostruisce pacchetti preservati
$ gentooupdate -r "@preserved-rebuild"
🧹 Fase 4 – Depclean
# 🧹 Rimuove pacchetti non più necessari
$ gentooupdate -d "--depclean"
🔧 Fase 5 – Revdep-Rebuild
# 🔧 Ricostruisce dipendenze rotte
$ gentooupdate -e ""
📝 Versione & Crediti
Gentoo Update 1.1.1.1

File originale: Nathan Shearer

Editore: Cristian Pozzessere

Licenza: GNU General Public License 3.0
