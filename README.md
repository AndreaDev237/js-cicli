# js-cicli

Esercizio da fare da soli, per il tutoraggio di mercoledì 18/11. Ripassi gli argomenti di martedì 17/11: il ciclo `for`, l'accumulatore, `while` e `do/while`. Servono anche le condizioni di sabato.

## Cosa devi fare

Otto tracce, ordinate dalla più facile alla più difficile. Ogni traccia è un piccolo programma legato a una situazione vera: le ripetizioni in palestra, l'ascensore, la cassa del supermercato…

Ogni traccia ha la sua pagina HTML e il suo file JavaScript, già collegati. **Scrivi solo nel file `.js`** della traccia: le pagine HTML non si toccano.

Le tracce da 1 a 5 si fanno con il `for`. Dalla 6 alla 8 non sai prima quante volte ripetere: lì serve il `while` (o il `do/while`). Fai le tracce in ordine: non devi finirle tutte stasera, si continua a casa.

## Prima di cominciare

- **Suggerimenti AI di Antigravity spenti**, come a lezione: con i cicli l'autocompletamento ti scriverebbe il `for` intero.
- **Niente Live Server.** Con `prompt` e `alert` la pagina si blocca e non si ricarica bene. Apri la pagina della traccia con **doppio clic** sul file `.html`, dalla cartella del progetto.
- Se il doppio clic apre un browser diverso da Chrome: tasto destro sul file, **Apri con** e scegli Google Chrome. Su Windows e su Mac il comando ha lo stesso nome.
- **Console sempre aperta**: F12, scheda Console. Su Mac Cmd+Opt+J.
- Dopo ogni modifica salva il file e premi **F5** nella pagina: il programma riparte da capo.
- **Se la scheda si blocca** o il `prompt` ricompare all'infinito, hai un ciclo infinito: la condizione non diventa mai `false`. Chiudi la scheda (se non basta, tutto il browser), correggi il file e riaprilo.

## Cosa trovi qui

```
├── 01-ripetizioni.html … 08-password.html   ← una pagina per traccia: si apre con doppio clic
├── bonus-1-ascensore-while.html, bonus-2-alto-basso.html
├── js/
│   ├── 01-ripetizioni.js                    ← qui scrivi il codice della traccia 1
│   ├── …
│   └── bonus-2-alto-basso.js
├── README.md                                ← questo file
└── AGENTS.md                                ← le istruzioni per il tutor AI
```

Perché una pagina per traccia: con un doppio clic parte solo il programma che ti interessa, e F5 lo rifà da capo. Non devi commentare e decommentare niente.

## Come lavori su ogni traccia

Ogni file `.js` contiene solo lo scheletro dei commenti. Dentro:

1. **Scrivi gli STEPS**: i passi del programma in italiano, uno per riga, prima di qualsiasi codice. Per ogni ciclo rispondi a tre domande: da dove parto, fino a quando giro, di quanto mi sposto?
2. **Scrivi il codice nelle quattro fasi**, sotto il commento giusto: preparazione, raccolta dati, elaborazione, output. Con un ciclo che chiede dati all'utente, il `prompt` sta dentro il ciclo: va bene se raccolta dati ed elaborazione finiscono lì dentro insieme.
3. **Se non sai cosa stamperà, fai la tabella dei giri** su un foglio: giro, valore del contatore, condizione, cosa fa il corpo.
4. **Apri la pagina** della traccia con doppio clic e prova **tutti** i casi di "Come verifichi".
5. **Fai un commit** quando la traccia funziona. Una traccia, un commit.

Il **Suggerimento** è chiuso: aprilo solo se resti bloccato.

## Come consegnare

1. Fai il **fork** di questa repo: bottone **Fork** in alto a destra, lascia il nome `js-cicli`. Il fork è la tua consegna: così il docente la vede.
2. Clona il **tuo** fork sul computer (`git clone` con l'indirizzo del tuo fork, non di questa repo) e apri la cartella in Antigravity.
3. Dopo ogni traccia: `git add`, `git commit` con un messaggio che dice quale traccia hai fatto, `git push` sul tuo fork.
4. Nessuna scadenza. Quando hai finito, incolla il link del tuo fork nel canale del corso.

---

## Le tracce

### 01 · Le ripetizioni

*Il `for` da 1 a 10.*

- **Obiettivo**: in palestra l'esercizio va fatto 10 volte. Stampa in console una riga per ogni ripetizione, da `Ripetizione 1` a `Ripetizione 10`. Alla fine, una volta sola, `Serie finita!`.
- **Come verifichi**:
  - in console ci sono 11 righe;
  - la prima è `Ripetizione 1` e l'ultima ripetizione è `Ripetizione 10`: non 0, non 11;
  - `Serie finita!` compare una volta sola, in fondo;
  - porta le ripetizioni a 15 cambiando **un solo numero**: ora le righe sono 16.

<details>
<summary>Suggerimento</summary>

Da dove parti, fino a quando giri, di quanto ti sposti? Se la serie parte da 0 o finisce a 11, fai la tabella dei giri e guarda la condizione: `<` o `<=`? Quello che si stampa una volta sola sta fuori dalle graffe. Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#giri), parte "Il for passo per passo".

</details>

### 02 · L'ascensore

*Il `for` da 0 a N, con `prompt`.*

- **Obiettivo**: chiedi a che piano vuoi andare. Mentre l'ascensore sale, stampa in console un piano per riga, dal piano terra: `Piano 0`, `Piano 1`… fino al piano scelto. Poi mostra con `alert` `Sei arrivato al piano 3`. Se l'utente non scrive un numero, o scrive un numero negativo, mostra solo `Piano non valido`: niente piani in console.
- **Come verifichi**:
  - 3 → in console `Piano 0`, `Piano 1`, `Piano 2`, `Piano 3`, poi l'alert `Sei arrivato al piano 3`;
  - 0 → solo `Piano 0`, poi `Sei arrivato al piano 0`;
  - `terzo` → `Piano non valido`, console vuota;
  - -2 → `Piano non valido`, console vuota;
  - Annulla → `Piano non valido`, console vuota.

<details>
<summary>Suggerimento</summary>

Il punto di arrivo del ciclo non lo scrivi tu: lo decide l'utente. Il ciclo parte solo se il piano è valido, quindi sta dentro un ramo dell'`if`. Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#pezzi), parte "Cambiare i tre pezzi", e dispensa [Condizioni](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-condizioni#number) per il controllo del numero.

</details>

### 03 · Il listino dei biglietti

*Il contatore entra nel calcolo.*

- **Obiettivo**: alla biglietteria del bus c'è un listino con il prezzo da 1 a 10 biglietti. Chiedi quanto costa un biglietto (in euro, senza centesimi) e stampa in console una riga per ogni quantità: `Quantità 1: 2 €`, `Quantità 2: 4 €`… fino a `Quantità 10: 20 €`.
- **Come verifichi**:
  - 2 → da `Quantità 1: 2 €` a `Quantità 10: 20 €`, 10 righe;
  - 3 → la riga 4 è `Quantità 4: 12 €` e l'ultima `Quantità 10: 30 €`;
  - `due` → 10 righe con `NaN` al posto del prezzo, da `Quantità 1: NaN €` in giù. Qui il prezzo non si controlla.

<details>
<summary>Suggerimento</summary>

È la tabellina di martedì: il contatore non serve solo a contare i giri, entra anche nel calcolo. Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#for), parte "Il ciclo for".

</details>

### 04 · Il coro dello stadio

*Ripetere una parola, e un accumulatore di stringhe.*

- **Obiettivo**: chiedi una parola del coro e quante volte ripeterla. In console stampa una riga per volta, numerata: `1 · Forza`, `2 · Forza`… Alla fine mostra con `alert` tutto il coro su una riga sola: `Forza Forza Forza`.
- **Come verifichi**:
  - `Forza` e 3 → in console `1 · Forza`, `2 · Forza`, `3 · Forza`; nell'alert `Forza Forza Forza` (se resta uno spazio in fondo, va bene);
  - `Olé` e 5 → 5 righe in console e 5 parole nell'alert;
  - `Forza` e 0 → console vuota e alert vuoto;
  - `Forza` e `tre` → console vuota e alert vuoto: sai dire perché il ciclo non parte?
  - Annulla sulla parola → al posto della parola compare `null`, cioè quello che restituisce `prompt`. Per ora va bene così.

<details>
<summary>Suggerimento</summary>

Il coro su una riga si costruisce come la somma di martedì, solo che al posto dei numeri attacchi stringhe: da quale valore parte, e dove lo dichiari? Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#accumulatore), parte "L'accumulatore".

</details>

### 05 · La media dei voti

*`prompt` dentro il `for`, accumulatore, `.toFixed()`.*

- **Obiettivo**: chiedi quanti voti hai preso, poi chiedi i voti uno alla volta. Ogni domanda dice quale voto stai scrivendo: `Voto 1 di 3`, `Voto 2 di 3`… Alla fine mostra con `alert` la media con un decimale: `Media: 7.3`. Se il numero di voti non è un numero o è minore di 1, mostra `Nessun voto da calcolare` senza fare altre domande. I singoli voti non li controlli: nelle prove scrivili sempre come numeri.
- **Come verifichi**:
  - 3 voti: 6, 7, 9 → `Media: 7.3`;
  - 2 voti: 6, 8 → `Media: 7.0`;
  - 1 voto: 10 → `Media: 10.0`;
  - 0 → `Nessun voto da calcolare`, nessun'altra domanda;
  - `tre` → `Nessun voto da calcolare`;
  - Annulla alla prima domanda → `Nessun voto da calcolare`.

<details>
<summary>Suggerimento</summary>

Dentro il ciclo chiedi un voto e lo aggiungi alla somma. La media si calcola **dopo** il ciclo, una volta sola. Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#accumulatore), parte "L'accumulatore", e dispensa [Variabili](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-variabili#properties) per `.toFixed()`.

</details>

### 06 · Il lucchetto

*`while` o `do/while`: ripeti finché…*

- **Obiettivo**: il lucchetto della bici si apre con la combinazione `482`. Chiedi la combinazione finché l'utente non la indovina. A ogni tentativo sbagliato stampa in console `Combinazione sbagliata, riprova`. Quando è giusta, mostra con `alert` `Lucchetto aperto!`.
- **Come verifichi**:
  - `111`, `999`, `482` → due righe `Combinazione sbagliata, riprova`, poi l'alert;
  - `482` al primo colpo → console vuota, subito l'alert;
  - campo vuoto, oppure Annulla → `Combinazione sbagliata, riprova`, e la domanda torna;
  - per uscire bisogna indovinare: se vuoi smettere prima, chiudi la scheda.

<details>
<summary>Suggerimento</summary>

Quante volte gira il ciclo? Non lo sai prima: è un lavoro per `while`. La domanda va **dentro** il ciclo, altrimenti la condizione non cambia mai e il ciclo è infinito. Siccome la domanda va fatta almeno una volta, guarda anche il `do/while`. Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#while), parti "Il ciclo while" e "Il ciclo do / while".

</details>

### 07 · La cassa del supermercato

*`while` con due accumulatori.*

- **Obiettivo**: alla cassa si battono i prezzi uno alla volta. Chiedi il prezzo di un prodotto (in euro, senza centesimi), poi un altro, finché il cassiere non scrive `0`. Se il prezzo non è un numero o è negativo, stampa in console `Prezzo non valido` e non contarlo. Alla fine mostra con `alert` quanti prodotti e il totale: `Prodotti: 3 · Totale: 23 €`. Lo `0` finale non è un prodotto.
- **Come verifichi**:
  - 5, 10, 8, 0 → `Prodotti: 3 · Totale: 23 €`;
  - 0 subito → `Prodotti: 0 · Totale: 0 €`;
  - 5, `dieci`, 10, 0 → in console `Prezzo non valido`, poi `Prodotti: 2 · Totale: 15 €`;
  - 5, -4, 0 → in console `Prezzo non valido`, poi `Prodotti: 1 · Totale: 5 €`;
  - Annulla, poi 7, poi 0 → in console `Prezzo non valido`, poi `Prodotti: 1 · Totale: 7 €`.

<details>
<summary>Suggerimento</summary>

Ti servono due accumulatori: uno per il totale e uno per contare i prodotti. Dentro il ciclo c'è un `if`: cosa fai con un prezzo valido, cosa con uno non valido, e cosa con lo `0`? Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#while), parte "Il ciclo while".

</details>

### 08 · La password in 3 tentativi

*Traccia difficile: due motivi per fermarsi.*

- **Obiettivo**: la password giusta è `segreta26`, e l'utente ha 3 tentativi. A ogni tentativo sbagliato stampa in console quanti tentativi restano: `Password errata. Tentativi rimasti: 2`. Se indovina entro 3 tentativi, mostra con `alert` `Benvenuto`. Se sbaglia 3 volte, mostra `Bloccato`, senza una quarta domanda. È un gioco: in un sito vero le password non si scrivono mai nel codice.
- **Come verifichi**:
  - `segreta26` al primo tentativo → `Benvenuto`, console vuota;
  - `ciao`, `segreta26` → `Tentativi rimasti: 2`, poi `Benvenuto`;
  - `ciao`, `prova`, `segreta26` → `Tentativi rimasti: 2` e `1`, poi `Benvenuto`;
  - `ciao`, `prova`, `boh` → `Tentativi rimasti: 2`, `1` e `0`, poi `Bloccato`. Nessuna quarta domanda;
  - Annulla tre volte → anche Annulla è un tentativo sbagliato: `Tentativi rimasti: 2`, `1` e `0`, poi `Bloccato`.

<details>
<summary>Suggerimento</summary>

Il ciclo deve fermarsi per due motivi diversi: la password è giusta, oppure i tentativi sono finiti. Quindi continua finché la password è sbagliata **e** ci sono ancora tentativi: due condizioni unite da un operatore logico. Dopo il ciclo, come fai a sapere per quale dei due motivi si è fermato? Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#while) e dispensa [Condizioni](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-condizioni#logical).

</details>

---

## Bonus (facoltativi)

Solo se hai finito le otto tracce. Stesse regole: STEPS, quattro fasi, doppio clic.

### Bonus 1 · L'ascensore con while

- **Obiettivo**: riscrivi la traccia 02 con un `while` al posto del `for`. Le uscite devono essere identiche.
- **Come verifichi**: gli stessi casi della traccia 02, con le stesse righe in console e gli stessi alert.

<details>
<summary>Suggerimento</summary>

I tre pezzi del `for` ci sono ancora tutti, solo sparsi: uno prima del ciclo, uno tra le tonde, uno in fondo al corpo. Quale? Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli#quale), parte "for o while?".

</details>

### Bonus 2 · Troppo alto, troppo basso

- **Obiettivo**: il computer pensa a un numero intero da 1 a 100. L'utente prova a indovinarlo: dopo ogni tentativo sbagliato stampa in console `Troppo alto` o `Troppo basso`. Se l'utente non scrive un numero (o preme Annulla), stampa `Scrivi un numero da 1 a 100`: conta lo stesso come tentativo. Quando indovina, mostra con `alert` in quanti tentativi: `Indovinato in 5 tentativi!`.
- **Come verifichi**: per provarlo stampa in console il numero segreto all'inizio, così sai cosa rispondere. Con il numero 40: 50 → `Troppo alto`, 30 → `Troppo basso`, 40 → `Indovinato in 3 tentativi!`. Con il numero 40: `boh`, 40 → `Scrivi un numero da 1 a 100`, poi `Indovinato in 2 tentativi!`. Quando funziona, togli la riga che stampa il numero segreto.

<details>
<summary>Suggerimento</summary>

È il lucchetto della traccia 06, con un numero a caso e un contatore dei tentativi. Il numero da 1 a 100 si fa come il numero casuale del pari o dispari di sabato, con `Math.floor`. La dispensa Cicli ha un esercizio finale simile, con la soluzione: guardala solo dopo averci provato da solo.

</details>

---

## Per ripassare

- Dispensa [Cicli](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-cicli) e dispensa [Condizioni](https://kb-aiwd.andreadev237.workers.dev/lezioni/js-condizioni).
- Quando un ciclo non fa quello che ti aspetti, fai la tabella dei giri prima di cambiare il codice.

Se usi l'AI, il file `AGENTS.md` la fa lavorare da tutor: ti fa domande e ti indica dove guardare, senza darti la soluzione.
