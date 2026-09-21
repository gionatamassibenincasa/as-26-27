# Markdown (GFM)

> **Guida rapida per studenti**
>
> Un'introduzione semplice e pratica per formattare i tuoi documenti ed appunti.

## 1. Enfasi del testo

Il Markdown permette di formattare il testo facilmente senza usare il mouse o menu complessi.

### Corsivo

Il testo in corsivo si scrive racchiudendolo tra singoli asterischi `*` o singoli trattini bassi `_`.

**Sintassi:**

```
*Questo testo è in corsivo*
_Anche questo è in corsivo_

```

**Risultato:**

*Questo testo è in corsivo*

*Anche questo è in corsivo*

### Grassetto

Il testo in grassetto si scrive racchiudendolo tra doppi asterischi `**` o doppi trattini bassi `__`.

**Sintassi:**

```
**Questo testo è in grassetto**
__Anche questo è in grassetto__

```

**Risultato:**

**Questo testo è in grassetto**

**Anche questo è in grassetto**

### Grassetto e Corsivo combinati

Per applicare entrambi gli stili, usa tre asterischi `***`.

**Sintassi:**

```
***Testo sia in grassetto che in corsivo***

```

**Risultato:**

***Testo sia in grassetto che in corsivo***

### Barrato (GFM)

In sintassi GFM, il testo barrato si ottiene racchiudendolo tra **doppie tilde** `~~` (su Windows: `Alt+126`, su Mac: `Option+5`).

**Sintassi:**

```
~~Questo testo è barrato~~

```

**Risultato:**

\~\~Questo testo è barrato\~\~

## 2. Capoversi e Interruzioni di riga

### Capoversi (Paragrafi)

Un capoverso include un insieme di frasi logicamente coese tra di loro. In Markdown, per separare due capoversi occorre lasciare **una riga vuota** (premere *Invio* due volte).

**Sintassi:**

```
Questo è il primo capoverso con alcuni concetti.

Questo è il secondo capoverso, ben separato dal precedente.

```

### Andare a capo nello stesso capoverso

Per andare a capo senza cambiare capoverso (ad esempio per una poesia o una strofa), inserisci **due o più spazi** alla fine della riga e poi premi *Invio*. In alternativa, puoi usare il tag HTML `<br>`.

**Sintassi:**

```
Si sta come  
d’autunno  
sugli alberi  
le foglie.

```

**Risultato:**

Si sta come

d’autunno

sugli alberi

le foglie.

## 3. Titoli e Struttura Logica

Un documento ben strutturato usa i titoli per organizzare i contenuti in livelli gerarchici. Per definire un titolo si usa il simbolo cancelletto `#` seguito da uno **spazio**.

Si possono usare da 1 a 6 cancelletti:

* `#` per il titolo principale (H1 - da usare generalmente una sola volta per documento);

* `##` per le sezioni principali (H2);

* `###` per i sottoparagrafi (H3), e così via.

**Sintassi:**

```
# Titolo di Livello 1 (H1)
## Titolo di Livello 2 (H2)
### Titolo di Livello 3 (H3)
#### Titolo di Livello 4 (H4)
##### Titolo di Livello 5 (H5)
###### Titolo di Livello 6 (H6)

```

## 4. Citazioni (Blockquotes)

Le citazioni sono utili per evidenziare testi estratti da altre fonti o citazioni d'autore. Si creano con il simbolo maggiore di `>` seguito da uno spazio.

**Sintassi:**

```
> Si sta come  
> d’autunno  
> sugli alberi  
> le foglie.  
>
> — *Soldati*, Giuseppe Ungaretti

```

**Risultato:**

> Si sta come
>
> d’autunno
>
> sugli alberi
>
> le foglie.
>
> — *Soldati*, Giuseppe Ungaretti

## 5. Elenchi

### Elenchi non ordinati (Puntati)

Si creano usando il trattino `-`, l'asterisco `*` o il più `+`, seguiti da uno spazio.

**Sintassi:**

```
- Primo elemento
- Secondo elemento
- Terzo elemento

```

**Risultato:**

* Primo elemento

* Secondo elemento

* Terzo elemento

### Elenchi ordinati (Numerati)

Si creano usando un numero seguito da un punto e uno spazio. Non occorre che i numeri siano sequenziali nel sorgente: Markdown li ordinerà automaticamente!

**Sintassi:**

```
1. Introduzione
2. Sviluppo
3. Conclusione

```

**Risultato:**

1. Introduzione

2. Sviluppo

3. Conclusione

### Elenchi annidati (Sotto-liste)

Per creare una sotto-lista, rientra gli elementi di **2 o 4 spazi** o usando il tasto *TAB*.

**Sintassi:**

```
1. Materie Scientifiche
   - Matematica
   - Fisica
2. Materie Umanistiche
   - Italiano
   - Storia

```

**Risultato:**

1. Materie Scientifiche

   * Matematica

   * Fisica

2. Materie Umanistiche

   * Italiano

   * Storia

### Liste di controllo / Task List (GFM)

Utilissime per to-do list e compiti a casa. Si creano con `- [ ]` per un elemento da completare e `- [x]` per un elemento completato.

**Sintassi:**

```
- [x] Leggere il capitolo 1
- [x] Fare gli esercizi di matematica
- [ ] Inviare la ricerca di storia

```

**Risultato:**

* \[x\] Leggere il capitolo 1

* \[x\] Fare gli esercizi di matematica

* \[ \] Inviare la ricerca di storia

## 6. Collegamenti Ipertestuali (Link)

### Automatici

Per convertire direttamente un indirizzo web in un link cliccabile, racchiudilo tra parentesi angolari `< >` (oppure in GFM incolla semplicemente l'URL completo).

**Sintassi:**

```
Visita il sito <https://www.wikipedia.org>.
```

**Risultato:**

Visita il sito <https://www.wikipedia.org>.

### Link in linea

Per associare un link ad un testo descrittivo, usa la sintassi `[Testo visibile](URL "Titolo Opzionale")`.

**Sintassi:**

```
Visita il sito del [Ministero dell'Istruzione](https://www.mim.gov.it "Sito Ufficiale MIM").

```

**Risultato:**

Visita il sito del [Ministero dell'Istruzione](https://www.mim.gov.it).

### Link con Riferimento

Utili quando si hanno molti link all'interno del documento per mantenere il codice sorgente ordinato.

**Sintassi:**

```
Consultare la [Documentazione GFM][gfm-docs] per maggiori dettagli, oppure il motore di ricerca [Google][google-ref].

[gfm-docs]: https://docs.github.com/en/get-started/writing-on-github
[google-ref]: https://www.google.com
```

## 7. Immagini

La sintassi per le immagini è identica a quella dei link, ma anticipata da un punto esclamativo `!`:
`![Testo alternativo](URL_immagine "Titolo opzionale")`.

**Sintassi:**

```
![Logo Markdown](https://markdown-here.com/img/icon256.png "Logo ufficiale Markdown")

```

**Risultato:**

*Suggerimento:* Se vuoi rendere un'immagine cliccabile, racchiudi il codice dell'immagine all'interno di un link:

```
[![Logo](https://markdown-here.com/img/icon256.png)](https://it.wikipedia.org/wiki/Markdown)

```

## 8. Codice informatico

### Codice in linea

Per citare brevi comandi, scorciatoie da tastiera o variabili all'interno di una frase, racchiudi il testo tra singoli **accenti gravi** `` ` `` (su Windows: `Alt+96`, su Mac: `Option+\`).

**Sintassi:**

```
Per salvare il file premi la combinazione `Ctrl + S`.

```

**Risultato:**

Per salvare il file premi la combinazione `Ctrl + S`.

### Blocchi di codice (Fenced Code Blocks)

Per inserire intere righe di codice o script, racchiudi il blocco tra tre accenti gravi prima e dopo. Nella sintassi GFM puoi specificare il linguaggio dopo i primi tre accenti gravi per attivare l'**evidenziazione della sintassi**.

**Sintassi:**

````
```python
# Esempio di codice Python
def saluta(nome):
    print(f"Ciao, {nome}!")

saluta("Classe")
```

````

**Risultato:**

```
# Esempio di codice Python
def saluta(nome):
    print(f"Ciao, {nome}!")

saluta("Classe")

```

## 9. Tabelle (GFM)

In GFM è possibile creare tabelle usando le barre verticali `|` per separare le colonne e i trattini `-` per separare l'intestazione.

I due punti `:` indicano l'allineamento del testo nella colonna:

* `:---` allineamento a sinistra (predefinito)

* `:---:` allineamento al centro

* `---:` allineamento a destra

**Sintassi:**

```
| Studente | Materia | Voto |
| :--- | :---: | ---: |
| Mario Rossi | Matematica | 8.5 |
| Luca Bianchi | Storia | 10.0 |
| Anna Verdi | Inglese | 9.0 |

```

**Risultato:**

| Studente | Materia | Voto |
| :--- | :---: | ---: |
| Mario Rossi | Matematica | 8.5 |
| Luca Bianchi | Storia | 10.0 |
| Anna Verdi | Inglese | 9.0 |

## 10. Avvisi e Note speciali / Callout (GFM)

GitHub supporta blocchi speciali di avviso per mettere in evidenza informazioni importanti. Si creano combinando le citazioni `>` con tag specifici come `[!NOTE]`, `[!TIP]`, `[!WARNING]`, ecc.

**Sintassi:**

```
> [!NOTE]
> Ricordati di consegnare l'elaborato entro venerdì.

> [!WARNING]
> Fai attenzione alla sintassi dei blocchi di codice!

```

**Risultato:**

> [!NOTE]
> Ricordati di consegnare l'elaborato entro venerdì.

> [!WARNING]
> Fai attenzione alla sintassi dei blocchi di codice!

## 11. Note a piè di pagina (GFM)

Puoi aggiungere note a piè di pagina inserendo un riferimento `[^1]` all'interno del testo e definendo poi la nota in un punto qualsiasi del documento.

**Sintassi:**

```
Ecco un'affermazione importante[^1] che richiede una nota di approfondimento.

[^1]: Questa è la nota spiegata a piè di pagina.

```

## 12. Matematica con sintassi LaTeX (GFM)

In GitHub Flavored Markdown è possibile inserire espressioni matematiche formattate usando la sintassi LaTeX.

### Matematica in linea (Inline)

Per inserire una formula all'interno del testo, racchiudila tra singoli simboli del dollaro `$`.

**Sintassi:**

```md
Un'equazione di secondo grado si presenta nella forma generica $ax^2 + bx + c = 0$ con $a \neq 0$.

```

**Risultato:**

Un'equazione di secondo grado si presenta nella forma generica $ax^2 + bx + c = 0$ con $a \neq 0$.

---

### Blocco di equazioni (Display mode)

Per formule più complesse o per evidenziare un'equazione al centro della pagina, racchiudi la formula tra **doppi simboli del dollaro** `$$`.

**Sintassi:**

```md
L'equazione risolutiva generale delle equazioni di secondo grado è:

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

```

**Risultato:**

L'equazione risolutiva generale delle equazioni di secondo grado è:

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
