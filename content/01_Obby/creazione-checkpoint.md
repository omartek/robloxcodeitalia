---
title: Creazione di checkpoint
weight: 30
tags: ["gameplay"] 
---

![checkpoint](IntroToStudio_heroCheckpoints.jpg)

## Creazione di checkpoint

Se fai un obby lungo, è frustrante per i giocatori arrivare quasi alla fine e poi cadere, perdendo tutti i loro progressi. Avere **più** posizioni di spawn come **checkpoint** consente al giocatore di rigenerarsi, o riavviarsi, dopo aver raggiunto determinate parti del gioco.

Le posizioni di spawn sono una buona idea nelle seguenti situazioni:

* **Prima** o **dopo** un salto difficile.
* Dopo che i giocatori hanno giocato per un breve periodo di tempo.

Impostazione del sistema di checkpoint  
Ogni giocatore ha una certa **SpawnLocation** assegnata. Ogni volta che il giocatore tocca una nuova spawn, la nuova posizione sostituisce quella vecchia. Se cade, si rigenererà **nell'ultima** posizione di spawn che ha toccato.

## Aggiungi il servizio di squadra

È possibile utilizzare uno strumento chiamato **Team Service** per creare più posizioni di spawn. Ogni squadra ha una posizione di spawn unica assegnata ad essa. Quando un giocatore cambia una squadra, cambia la sua posizione di spawn .

1. Seleziona la scheda Modello.
1. Nella sezione **Avanzate** (più a destra), fai clic su **Servizio** (due ingranaggi).
![inserisci service](InsertService_updated.png)
1. Seleziona **Teams** .
1. Fai clic su **Inserisci**.
![inserisci team](TeamsInsert_480x320.png)
1. Verifica di avere una cartella **Teams** in **Explorer**.
![team creato](TeamsCreated_480x320.png)

### Aggiungi una squadra

Con il servizio Team aggiunto, puoi creare team. Ricorda, ogni squadra che crei sarà in realtà una posizione di spawn **diversa** (checkpoint) nel tuo obby. Durante il gioco, il giocatore cambierà squadra per **cambiare** la posizione di spawn più recente.

1. In **Explorer**, fare clic con il pulsante destro del mouse su **Teams**.
1. Fai clic su **Inserisci** oggetto> **Team** . Verrà creato un nuovo team nella cartella Teams.
![nodo team](TeamNode_480x320.png)

### Rinomina la squadra

Piuttosto che avere un **nome di squadra**, vogliamo un **nome di area**. Il nome dovrebbe corrispondere al tema del tuo gioco. Di seguito sono riportati alcuni esempi di nomi:

* Valle dell'unicorno
* Area del villaggio
* Dojo per principianti

Effettua le seguenti operazioni per rinominare il team:

1. Fai clic con il pulsante destro del mouse su **Team**.
1. Seleziona **Rinomina**.
![rinomina team](RenameTeamNode_480x320.png)
1. Aggiungi un nome descrittivo.

## Modifica delle spawn della squadra

All'inizio, qualsiasi squadra può utilizzare solo la SpawnLocation originale. Anche se suona come una buona cosa, un giocatore nella tua 15a posizione di spawn potrebbe rigenerarsi accidentalmente all'inizio dell'intero gioco.

### Imposta proprietà squadra

Per risolvere questo possibile problema, dobbiamo modificare le proprietà del team.

1. Fai clic su SpawnLocation iniziale .
1. Nella finestra Proprietà , deseleziona Neutro.
![uncheck neutral](UncheckNeutral_480x320.png)

Ora i giocatori possono comparire in questa SpawnLocation **solo se corrispondono** al TeamColor della SpawnLocation. Ciò eviterà certi problemi che potremmo avere nel nostro gioco.

### Assegna la squadra al primo SpawnLocation

Affinché una squadra e un SpawnLocation corrispondano, il **Team Color** e **SpawnLocation** devono corrispondere esattamente.

1. Nella finestra della proprietà SpawnLocation, cerca **TeamColor**; dovrai ricordare questo colore.
1. Fai clic sull'oggetto Team che hai rinominato.
1. Imposta il **TeamColor** in modo che corrisponda al primo SpawnLocation.
1. Metti alla prova il tuo gioco.

{{% notice tip %}}
SpawnLocation non funziona?
Se SpawnLocation non funziona, controlla quanto segue:  
:  
* Assicurati di sostituire il TeamColor, non il BrickColor di SpawnLocation.
* Controlla che i colori corrispondano esattamente.
{{% /notice %}}

## Aggiunta di altre posizioni di spawn

Ora puoi iniziare il processo di aggiunta di più posizioni di spawn per offrire al tuo giocatore un'esperienza più lunga e più interessante.

### Imposta SpawnLocation

1. Crea un nuovo SpawnLocation.
1. Rinomina SpawnLocation *SpawnLocation2*.
1. Seleziona *AllowTeamChangeOnTouch*. Ora ogni volta che qualcuno tocca SpawnLocation, si unirà al colore della squadra corrispondente.
1. Deseleziona **Neutro** .
1. Scegli un nuovo **TeamColor**.
![SpawnLocation2](SpawnLocation2_480x320.png)

### Imposta l'oggetto team

1. Crea un nuovo oggetto team (fai clic con il pulsante destro del mouse su Teams> Inserisci oggetto> Team).
1. Rinominalo con il nome della tua area. Ad esempio *Goat Mountain*.

### Modifica le proprietà della squadra

1. Deseleziona **AutoAssignable**.
1. Cambia **TeamColor** in modo che **corrisponda** al nuovo SpawnLocation.
![team2](Team2_480x320.png)

Solo il primo team deve essere impostato su **AutoAssignable**. In questo modo i giocatori verranno automaticamente assegnati al **primo** checkpoint quando iniziano il gioco.

## Continua il tuo progetto

1. Aggiungi **almeno 3** nuove posizioni di spawn.
1. Dopo aver aggiunto ogni punto, verifica che funzioni come previsto.

Puoi aggiungere molte posizioni di spawn, ma assicurati di:

* Rinomina ognuno in qualcosa di diverso (ad esempio, SpawnLocation2, SpawnLocation3 ...)
* Usa un **colore di squadra** diverso per ogni posizione di spawn / oggetto di squadra.

{{% notice tip %}}
Il giocatore non viene generato correttamente?
Controlla per assicurarti che tutte le seguenti condizioni siano vere:

* Solo il primo team è impostato su AutoAssign.
* SpawnLocation è contrassegnato come neutro.
* Il colore corrisponde a SpawnLocation TeamColor e all'oggetto Team TeamColor.
{{% /notice %}}
