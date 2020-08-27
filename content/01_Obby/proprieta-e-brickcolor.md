---
title: Proprietà e Brickcolor
weight: 45
tags: ["coding base"] 
---

## Proprietà e BrickColor

Le **proprietà** controllano l'aspetto e il funzionamento degli oggetti. Alcune proprietà che un oggetto potrebbe avere sono materiale, colore o forma. Gli **script possono modificare** le proprietà, come fare in modo che una parte cambi colore.

## La finestra delle proprietà

Molte delle proprietà di un oggetto vengono visualizzate nella finestra **Proprietà**. Per vedere alcune proprietà già utilizzate dagli oggetti nel tuo gioco:

* Seleziona una parte.
* Scorri la finestra delle proprietà in basso a destra.

{{% notice tip %}}
Non riesci a vedere la finestra delle proprietà?  
Se non vedi la finestra Proprietà, fai clic sulla scheda **Visualizza** e quindi sul pulsante Proprietà.
{{% /notice %}}

## Modifica delle proprietà

Lo script utilizzerà il codice per cambiare il colore di una parte all'inizio del gioco.

![cambia colore gif](cambia-colore.gif)

### Imposta la parte e lo script

* Seleziona una parte esistente o creane una nuova.
* Rinomina la parte. Questo esempio usa *PracticePart*.
* Rinomina lo script *ChangeBrickColor*.
* Elimina `Hello World`.

### Crea un commento

Dovresti sempre iniziare nuovi script con un commento su ciò che fa lo script. I **commenti** sono righe speciali che aiutano i programmatori a ricordare a cosa servono gli script ma che non vengono eseguiti.

1. Scrivi `--` e una nota su cosa fa questo script. Il testo dovrebbe diventare verde per farti sapere che è un commento.
> -- Cambia il colore di PracticePart

### Individua la parte

Per apportare modifiche a qualsiasi parte utilizzando il codice, lo script deve prima sapere con quale parte lavorare. Usa Explorer per trovare la posizione della parte. In questo caso, PracticePart si trova in Workspace.

Ora che sai che PracticePart si trova in Area di lavoro, trasforma queste informazioni in codice comprensibile dal programma.

Digita gamequi sotto il tuo commento.

- Cambia il colore di PracticePart
gioco

Usa i punti per separare le parole. Sulla stessa riga, digitare .seguito da Workspace, la posizione della parte.

- Cambia il colore di PracticePart
gioco . Area di lavoro

Utilizzo del completamento automatico

Roblox completerà automaticamente le parole durante la digitazione per accelerare il processo di codifica. Quando vengono visualizzate le parole, puoi utilizzare i tasti freccia per spostarti verso il basso nell'elenco. Scegli un'opzione premendo Enter.

Completa la riga con il nome della parte come nell'esempio sotto.

- Cambia il colore di PracticePart
gioco . Area di lavoro . PracticePart

Controlla il tuo codice prima di proseguire

Assicurati che il tuo codice sia esattamente come il codice sopra e che PracticePart sia scritto e in maiuscolo esattamente come in Explorer.

## Modifica di una proprietà con il codice

Quasi lì! Ora cambierai il colore della parte con la BrickColorproprietà.

Digitare .BrickColordopo il nome della vostra parte.

- Cambia il colore di PracticePart
gioco . Area di lavoro . PracticePart . BrickColor

### Utilizzo dei valori RGB

Per modificare la BrickColorproprietà, crea un nuovo BrickColor per sostituire quello corrente. Tuttavia, non è come mescolare i colori, i programmi usano valori RGB , la combinazione di rosso, verde e blu per creare tutti i colori sullo schermo.

Esistono alcune regole per l'utilizzo dei valori RGB:

Usa 3 numeri decimali; uno per ogni colore.
Separa ogni numero con una virgola.
Usa numeri compresi tra 0 e 1. 0 significa che un colore è completamente fuori. 1 significa che il colore è completamente acceso.

Di seguito sono riportati alcuni esempi di valori RGB:
Colore 	Codice
BrickColor.new(0.9,0.6,0.2)
BrickColor.new(0.2,0.6,0.2)
BrickColor.new(0.8,0.2,0.8)

### Crea un nuovo colore RGB

Ora utilizzerai il =segno per impostare un nuovo colore per sostituire il colore della parte originale. Puoi usare i numeri decimali per i colori nella tabella sopra o crearne uno tuo.

Dopo game.Workspace.PracticePart.BrickColor: digitare= BrickColor.new()

- Cambia il colore di PracticePart
gioco . Area di lavoro . PracticePart . BrickColor = BrickColor.new ( 0.9 , 0.8 , 0.1 ) 

All'interno delle parentesi, aggiungi 3 numeri decimali (compresi tra 0 e 1), separati da virgole. Ricorda, questo è il valore del colore RGB della tua parte.

- Cambia il colore di PracticePart
gioco . Area di lavoro . PracticePart . BrickColor = BrickColor.new ( 0.9 , 0.8 , 0.1 ) 

Premi Riproduci per verificare che la tua parte cambi colore.

Suggerimenti per la risoluzione dei problemi »

Problema : la parte è ancora grigia o non cambia colore come previsto

Assicurati di aver seguito tutte e tre le regole per i valori RGB (il numero è 0-1, è un decimale, tutti i numeri separati da virgole).
Se stai facendo numeri casuali, potresti ottenere un colore a sorpresa.

Suggerimenti generali

Verifica che le lettere maiuscole e minuscole e l'ortografia siano le stesse dell'esempio di codice. Brickcolornon funzionerà, mentre BrickColorfunzionerà.

