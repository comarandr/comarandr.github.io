# BASE DI GIT

## Creare una repository

`git init` : Crea una nuova repository Git nella directory corrente
`git clone <url>` : Clona una repository esistente da un URL. Imposta automaticamente il tracciamento del branch remoto "origin" e del branch "master" (o "main")

## Salvare le modifiche

**area di staging** : è una zona temporanea dove si preparano i file prima di eseguire un commit

`git add <file>` : Aggiunge un file specifico all'area di staging

`git add .` : Aggiunge tutti i file modificati all'area di staging

`git commit -m "messaggio"` : Crea un commit con i file presenti nell'area di staging e un messaggio descrittivo

`git commit` : Apre l'editor predefinito per inserire un messaggio di commit dettagliato (riassunto + descrizione)

`git status` : Mostra lo stato dei file nella directory di lavoro (branch attivo, file modificati, file in staging, file non tracciati)

## Creare nuovi branch

`git branch` : Elenca i branch locali

`git branch <nome-branch>` : Crea un nuovo branch con il nome specificato

- `git branch -d <nome-branch>` : Elimina un branch (deve essere già unito o non avere modifiche non salvate)
- `git branch -D <nome-branch>` : Forza l'eliminazione di un branch anche se non è stato unito

`git switch [options] <nome-branch>` : Passa al branch specificato

- `git switch -c <nome-branch>` : Crea un nuovo branch e passa ad esso
  - `git switch -c name <base-branch>` : Crea un nuovo branch basato su altro branch e passa ad esso
- `git switch -` : Passa al branch precedente
- `git switch --detach <commit>` : Passa a un commit specifico in modalità detached HEAD (non associato a un branch)

`git checkout <nome-branch>` : Passa al branch specificato (spesso sostituito da switch)

- `git checkout -b <nome-branch>` : Crea un nuovo branch e passa ad esso
- `git checkout -d <nome-branch>` : Elimina un branch

## Spostarsi tra i commit

### visualizzare la cronologia dei commit

`git log` : Mostra la cronologia dei commit

`git log --oneline` : Mostra la cronologia dei commit in formato compatto (una riga per commit)

`git log --graph` : Mostra la cronologia dei commit con una rappresentazione grafica dei branch e dei merge

`git log --all` : Mostra la cronologia dei commit di tutti i branch

`git log --remote` : Mostra la cronologia dei commit dei branch remoti

### spostarsi in un commit specifico

`git checkout <commit>` : Passa a un commit specifico (modalità detached HEAD)

`git switch --detach <commit>` : Passa a un commit specifico in modalità detached HEAD (alternativa a checkout)

`git checkout <nome-branch>^` : Passa al commit genitore del branch specificato

`git checkout <nome-branch>~n` : Passa al commit n livelli sopra il branch specificato

### operatori di riferimento ^ e ~

- `^` : Riferisce al genitore di un commit
  - `^<numero>` : Riferisce al genitore n-esimo di un commit nel caso di genitori multipli (**spostamento orizzontale**)
- `~` : Riferisce al commit genitore di un commit, ma permette di specificare un numero di livelli da risalire
  - `~n` : Riferisce al commit n livelli sopra il commit specificato (**spostamento verticale**)

Gli operatori `^` e `~` possono essere combinati per navigare nella cronologia dei commit

### forzatura di un branch

`git branch -f <nome-branch> <commit>` : Forza il branch a puntare a un commit specifico (può causare perdita di dati se non usato con cautela)

- nota: \<commit> può anche essere un riferimento relativo `nome-branch~n` o `nome-branch^`

## Unire i branch

`git merge <nome-branch>`: Unisce il branch specificato nel branch attivo

in assenza di conflitti non sarà necessario risolvere manualmente le modifiche

`git rebase <nome-branch>`: Applica le modifiche del branch attivo sul il branch specificato (se mi trovo su B e faccio `rebase A` applica le modifiche di B su A)

1. creo il ramo secondario con la feature da sviluppare
2. mi sposto sul ramo secondario e faccio i commit
3. mentre sono sul ramo secondario, faccio un rebase del ramo principale per portare le modifiche più recenti
4. risolvo eventuali conflitti

- pro: mantiene una cronologia più lineare e pulita
- contro: modifica lo storico dei commit

## Annullare le modifiche

`git reset <commit>` : Resetta il branch attivo a un commit specifico, annullando tutte le modifiche successive (perdita di dati)

`git revert <commit>` : Crea un nuovo commit che annulla le modifiche introdotte da un commit specifico (non altera la cronologia)

**nota**: \<commit> è il commit a cui si vuole tornare

## git cherry-pick

`git cherry-pick <commit>` : Applica le modifiche introdotte da un commit specifico al branch attivo (utile per portare modifiche specifiche da un branch all'altro senza unire tutto il branch)

`git rebase -i <nome-branch/commit>` : apre un editor interattivo che ti permette di selezionare i commit da includere, moficare o eliminare durante un rebase, dal branch o commit specificato fino al branch attivo.

## Git tag

`git tag <nome-tag>` : Crea un tag leggero con il nome specificato, permette di identificare un commit preciso

`git describe <ref>` : Mostra una descrizione del commit più vicina a un tag, con output del tipo `<tag>-<numero-commit>-g<hash>`

## Sincronizzare con un repository remoto

### scaricare da un repository remoto

**nota**: i rami remoti riflettono lo stato del repository remoto dall'ultima volta che abbiamo comunicato con esso (tramite fetch, pull o push)

`git clone` : Clona una repository esistente da un URL, creando una copia locale del repository remoto

`git fetch`: scarica commit presenti in remoto e assenti dal nostro repository locale, aggiornando dove puntano i nostri branche remoti ("origin/branch") ma senza modificare i nostri branch locali. è una sorta di download dei cambiamenti.

`git remote add <nome-remoto> <url>` : Aggiunge un repository remoto con un nome specificato

**nota**: potenzialmente è possibile prima scaricare i commit con fetch e poi unirli e spostarsi attraverso essi come se fossero stati creati localmente (cherry-pick, merge, rebase, checkout ... <origin/master>)

### scaricare e modificare direttamente

`git push <remoto> <place>` : Invia i commit del branch locale al repository remoto

`git push <remoto> <branch-locale>:<branch-remoto>` : Invia i commit del branch locale al repository remoto, specificando il nome del branch remoto (se diverso da quello locale)

`git pull <nome-remoto> <nome-branch>` : Recupera e unisce i cambiamenti dal repository remoto al branch locale, consiste nella combinazione di `git fetch` e `git merge`

**nota**: generalmente il main branch è bloccato. Normalmente bisogna:

1. creare un branch secondario
2. fare le modifiche e i commit su questo branch
3. fare un push del branch secondario al repository remoto
4. creare una pull request per unire le modifiche al main branch

## Tracking

`git branch -u <nome-remoto>/<branch-remoto> <branch-locale>` : Imposta il tracking del branch remoto con il branch locale. Se stiamo lavorando giù sul branch locale possiamo ometterlo

`git checkout -b <branch-locale> <nome-remoto>/<branch-remoto>` : Imposta il tracking del branch remoto con il branch locale
