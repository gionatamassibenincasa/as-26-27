# Appunti Git

## Cos'è GIT

`Git` è uno strumento per la gestione dei progetti, in particolare dei progetti software. Fa parte della categoria dei sistemi *Source Control Management* (SCM).

## Cos'è un repository

Un *repository* (letteralmente *deposito*, archivio storico) contiene tutti i *file* (documento digitale) del progetto e la cronologia delle revisioni di ogni file.
È possibile usare i repository per gestire il lavoro, tenere traccia delle modifiche, archiviare la cronologia delle revisioni e collaborare con altri utenti.

### Come creare un repository

Se si ha installato il programma `git` nel proprio *computer*, si può invocare il programma da riga di comando (*shell* o *prompt* o *terminale*), si usa:

```sh
git init
```
Il comando crea una *directory* (cartella) di nome `.git` che conterrà tutte le informazioni sul progetto.

### Come clonare un repository

Per scaricare una copia locale di un repository remoto già esistente, si usa il comando:

```sh
git clone <URL_del_repository>
```
Questo comando scarica i file del progetto e l'intera cronologia delle revisioni nella cartella di lavoro.

### Come aggiungere un file al repository

Per tracciare un nuovo file o preparare le modifiche per il salvataggio (*staging area*), si usa:

```sh
git add <nome_file>
```
Per aggiungere contemporaneamente tutti i file nuovi o modificati presenti nella cartella corrente:

```sh
git add .
```

## Concetti chiave

### Cos'è la HEAD

La **HEAD** è un puntatore speciale che indica la posizione corrente all'interno della cronologia del repository. Nella maggior parte dei casi, punta al ramo attivo (e quindi al suo commit più recente). Quando ci si sposta tra i vari rami o commit, Git sposta il puntatore HEAD per far riflettere il nuovo stato nella *working directory*.

## Gestione dei rami e spostamento

### `git branch`

Consente di gestire i rami del progetto.
* `git branch`: mostra l'elenco dei rami locali e indica qual è quello attivo.
* `git branch <nome_ramo>`: crea un nuovo ramo partendo dal commit corrente.
* `git branch -d <nome_ramo>`: elimina il ramo specificato (solo se le modifiche sono già state integrate).

### `git switch`

È il comando moderno (introdotto in Git 2.23) dedicato esclusivamente al cambio di ramo, per evitare l'ambiguità del comando `git checkout`.
* `git switch <nome_ramo>`: passa al ramo specificato.
* `git switch -c <nome_ramo>`: crea un nuovo ramo e vi si sposta immediatamente.

### `git checkout`

Comando versatile e storico di Git usato per navigare tra i rami o ripristinare lo stato di file della *working directory*.
* `git checkout <nome_ramo>`: passa al ramo indicato.
* `git checkout -b <nome_ramo>`: crea un nuovo ramo e vi si sposta.
* `git checkout <commit>`: sposta la HEAD su un commit specifico (stato di *detached HEAD*).
* `git checkout -- <nome_file>`: ripristina il file allo stato dell'ultimo commit, annullando le modifiche locali.

## Integrazione delle modifiche

### `git merge`

Unisce la cronologia di un ramo secondario nel ramo attivo corrente. Genera un nuovo commit (detto *merge commit*) che ha due genitori e mantiene inalterata la struttura ad albero della cronologia originale.
```sh
git merge <nome_ramo>
```

### `git rebase`

Prende i commit creati sul ramo corrente e li "riapplica" uno ad uno sopra la cima di un altro ramo. A differenza del merge, il rebase **riscrive la cronologia** creando nuovi commit, offrendo un flusso di lavoro con una cronologia lineare e pulita.
```sh
git rebase <nome_ramo>
```

## Gestione dei ripristini e annullamenti

### `git reset`

Sposta il puntatore del ramo attivo (e della HEAD) a un commit precedente. Viene usato principalmente per annullare modifiche locali non ancora condivise sul repository remoto.
* `git reset --soft <commit>`: annulla i commit successivi ma mantiene le modifiche nell'area di *staging*.
* `git reset --mixed <commit>`: comportamento predefinito; annulla i commit e lo *staging*, lasciando le modifiche nella *working directory*.
* `git reset --hard <commit>`: elimina definitivamente tutte le modifiche successive, sia dallo *staging* sia dalla *working directory*.

### `git revert`

Annulla le modifiche introdotte da un commit specifico creando un **nuovo commit opposto**. Non altera la cronologia passata, rendendolo il comando sicuro per annullare modifiche in rami pubblici o remoti già condivisi con il team.
```sh
git revert <hash_commit>
```

## Flusso di lavoro

### Che cosa sono i commit

Un *commit* è un'istantanea (*snapshot*) dello stato del progetto in un determinato momento. Salva in modo permanente nella cronologia di Git le modifiche precedentemente aggiunte allo staging. Si esegue con:

```sh
git commit -m "Messaggio descrittivo delle modifiche"
```

### Che cosa sono le pull request

Una *Pull Request* (PR) — o *Merge Request* — è una richiesta di integrazione delle modifiche da un ramo secondario al ramo principale del progetto. Permette agli altri membri del team di revisionare il codice (*code review*) prima che venga unito.

### Flusso GIT

Il flusso di lavoro tipico in Git si articola in quattro fasi:

1. **Working Directory**: la cartella locale in cui si modificano fisicamente i file.
2. **Staging Area**: l'area di preparazione in cui si selezionano i file da salvare con `git add`.
3. **Local Repository**: il repository locale in cui il salvataggio viene registrato con `git commit`.
4. **Remote Repository**: il server remoto dove si inviano i commit con `git push` o si sincronizzano le modifiche con `git pull`.

## GitHub

### Cosa è GitHub

`GitHub` è una piattaforma web di hosting per repository Git. Offre un'interfaccia grafica per esplorare il codice e aggiunge strumenti avanzati di collaborazione, gestione degli accessi, automazione (GitHub Actions) e tracciamento delle attività.

### Cosa sono le Issue

Le *Issue* sono schede di tracciamento utilizzate su GitHub per segnalare bug, proporre nuove funzionalità, distribuire compiti (*task*) o avviare discussioni relative al progetto.
