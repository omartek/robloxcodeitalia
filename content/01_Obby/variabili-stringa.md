---
title: Variabili stringa
weight: 40
tags: ["coding base"] 
---

## Variabili stringa

Ogni volta che crei un nuovo script, nella parte superiore dell'editor di script, compare l'istruzione print. La **funzione print** visualizza il testo sullo schermo. È una delle prime funzioni che molte persone imparano poiché è un modo semplice per dare un comando allo script.

Di seguito è riportato un esempio della funzione di stampa digitata e del suo output, ciò che vedrai una volta eseguito lo script.

|Esempio di codice|Uscita prevista|
|-----------------|---------------|
| `print ("Hello world!")`|Hello world!|

## Tipi di variabili - Stringhe

`"Hello World"` è un tipo di variabile stringa. **Le variabili** sono contenitori di informazioni che il programma può utilizzare e modificare, come nomi o punti dei giocatori.

Esistono molti tipi di variabili. Le variabili **stringa** contengono una **combinazione** di lettere e numeri. Sono usati per memorizzare informazioni come i nomi. Variabili di tipo Stringa sono sempre racchiuse all'interno delle virgolette, `"così"`.

Esempi di stringhe:

* `"You just joined the game!"`
* `"There are 50 players left"`
* `"10"`

## Codifica il tuo messaggio

Invece di dire `Hello World`, crea il tuo messaggio modificando la stringa nella funzione print.

1. In Explorer, passa il mouse su **ServerScriptService**. Fai clic sul + e selezionare **Script**.
![aggiungi script](ServerScriptServiceAddScript_2A_280x310.png)
1. Nell'editor degli script, sostituisci `"Hello World"` con una stringa che includa il tuo animale preferito.

|`print ( "I porcospini sono i miei animali preferiti." )`|

## Test di output

Per testare il codice, utilizzare la **finestra di output**. Questa finestra mostra l'output di stampa e gli errori degli script.

Per aprire la finestra di output e testare lo script:
1. Seleziona la scheda del menu **View (visualizza)** .
1. Fai clic su **Output**. La finestra apparirà nella parte inferiore di Roblox Studio.
![pulsante output](Output_480x320.png)
1. Per provare lo script, premi **Play**. La nuova stringa verrà visualizzata nella finestra di output.
![esecuzione script](showScriptRunning.png)
1. Poiché hai testato lo script, interrompi con lo **Stop** il playtest. Ora puoi tornare alla scheda Script per apportare ulteriori modifiche o testare altre stringhe.

{{% notice tip %}}
Manca la scheda dello script?
Se non vedi l'editor di script, fai doppio clic sul nome dello script in Explorer per riaprire lo script.
{{% /notice %}}

## Risoluzione dei problemi relativi al codice

Non importa da quanto tempo scrivi programmi, a volte le cose non funzionano al primo tentativo. Il **troubleshooting** o **risoluzione dei problemi** è il processo di ricerca, nel codice, per trovare e risolvere i problemi.

Se il tuo codice non ha funzionato:

* Assicurati che `print` sia minuscolo.
* La stringa è circondata da virgolette: `"così"`.
* La stringa è all'interno delle parentesi: `("così")`.
* Chiedi aiuto a un amico o prova a ripetere il tuo lavoro dall'inizio.

### Crea un errore

Per capire meglio che aspetto hanno gli errori, crea di proposito un errore.

1. Apri lo script.
1. Elimina le virgolette dall'istruzione print.
1. Passa il mouse sulla **linea rossa** per visualizzare un messaggio di errore. In questo caso, dovresti leggere `Unfinished string` che significa che la stringa manca di virgolette.

![linea rossa](ErrorRedline_480x320.png)

### Leggi un errore

I messaggi di errore vengono visualizzati come linee rosse sia nell'editor di script che nella finestra di output. È possibile utilizzare questi messaggi di errore per individuare il problema.

1. Premi **Play** per eseguire il codice.
1. Nota l'errore rosso nella **finestra di output**. Ogni errore ha una descrizione unica. In questo caso, una "malformed string" significa che alla stringa manca qualcosa.
1. Fai clic sul **messaggio rosso** nella finestra di output; questo ti porterà dove si trova l'errore nel tuo codice.

|Esempio di codice|Uscita prevista|
|-----------------|---------------|
|`print("this code doesn't work)|11:20:03.840 - ServerScriptService.Script:1: Expected identifier when parsing expression, got malformed string|


