---
title: Loop e Brickcolor
weight: 50
tags: ["coding base"] 
---

## Loop e BrickColor

Le parti non devono essere limitate a un solo colore. Possono scorrere un elenco dei tuoi colori preferiti per creare una foresta per unicorni o un tributo alla tua squadra sportiva preferita.

Fai ripetere il codice usando un ciclo (detto anche loop) `while true do`. Questo tipo di ciclo viene eseguito finché qualcosa non gli dice di fermarsi. Dato che non diremo al codice di fermarsi, funzionerà per sempre!
![loop colori](loop-colori.gif)

### Imposta una parte e uno script

1. Crea una nuova **parte** con un nome descrittivo. Questa lezione usa *LoopingPart* .
1. In **ServerScriptService**, aggiungi un nuovo script denominato *LoopingScript*.
1. Nello script, elimina `Hello World` e scrivi un commento che dichiari lo scopo di questo script.

```lua
-- Cambia il colore di LoopingPart ogni pochi secondi
```

## Utilizzo di variabili

Le variabili possono contenere anche altro oltre alle stringhe, per esempio un intero oggetto.

Piuttosto che digitare `game.Workspace.NameOfYourPart` più e più volte, l'intera riga può essere memorizzata all'interno di una **variabile locale**. Le variabili locali vengono create digitando local e quindi il nome della variabile, ad esempio `local nameOfVariable`

Una **variabile locale** funziona solo nello script in cui è stata creata. La maggior parte delle variabili che utilizzi saranno variabili locali.

1. Sotto il commento, crea una **variabile locale** denominata `loopingPart` digitando `local loopingPart`.
1. Impostare la variabile sulla parte che eseguirà il ciclo digitando `= game.Workspace.loopingPart` sulla stessa riga.

```lua
-- Cambia il colore di LoopingPart ogni pochi secondi
local loopingPart = game.Workspace.LoopingPart
```
{{% notice tip %}}
Utilizzando il segno di uguale  
In informatica, il segno `=` non ha lo stesso significato che ha in matematica. Non significa che due entità sono uguali. Invece, assegna il valore a una variabile.
{{% /notice %}}

{{% notice tip %}}
Regole di denominazione - Variabili e parti  
Gli sviluppatori Roblox hanno regole quando nominano parti e variabili per aiutarli a distinguere velocemente cos'è una variabile e cos'è una parte.  
<strong>Parti :</strong> PascalCase (prima lettera maiuscola)  
Esempi: <em>LoopingPart</em>, <em>EndZone</em>  
<strong>Variabili:</strong> camelCase (prima lettera minuscola)  
Esempi: <em>loopingPart</em>,<em>playerHealth</em>
{{% /notice %}}

## Crea un ciclo while true do

Ora, creerai il ciclo `while` che conterrà tutto il codice che dovrebbe ripetersi.

1. Nella riga successiva digita `while true do`.
1. Premi `Enter`. La parola `end` dovrebbe comparire automaticamente.

```lua
-- Changes the color of loopingPart every few seconds
local loopingPart = game.Workspace.LoopingPart
    
-- Looping Code
while true do

end
```

{{% notice tip %}}
Codice di rientro  
Potresti aver notato che l'editor aggiunge automaticamente <em>end</em> allo script e rientra a destra la riga di codice successiva. Il rientro rende il codice più facile da leggere.
{{% /notice %}}

#### Aggiungi codice all'interno del ciclo

Tutto ciò compreso `while true do` e `end` andrà in loop per sempre. All'interno del ciclo, aggiungi una riga di codice per ogni colore.

1. Tra `while true do` e `end`, cambia la proprietà BrickColor della parte in loop.

```lua
-- Changes the color of loopingPart every few seconds
local loopingPart = game.Workspace.LoopingPart
    
-- Looping Code
while true do
    -- Changes loopingPart's color
    loopingPart.BrickColor = BrickColor.new(0.7, 0.9, 0.9)
end
```

{{% notice warning %}}
<strong>Non eseguire ancora lo script</strong>  
Se esegui lo script ora, riceverai un errore. Questo perché lo script cambia i colori così velocemente, causando il sovraccarico di Studio. Affronterai questo problema in seguito facendo attendere lo script dopo ogni cambio di colore.
{{% /notice %}}

### Mantieni il codice nell'ambito (scope)

Affinché il codice possa essere eseguito nel ciclo, deve essere compreso tra `while true do` e `end`. Quando il codice è nel posto giusto, in modo che venga eseguito correttamente, viene detto nello **scope**.

```lua
-- Looping Code
while true do
        -- Inside of the loop's scope. This code will run forever.
end
-- Outside of the loop's scope. This code will never run.
```

## Far aspettare lo script

Se aggiungi subito una seconda riga di codice che cambia colore, cambierà il colore del mattone così velocemente che potresti non vedere nemmeno il primo colore passare. Per fare in modo che lo script attenda prima di eseguire la riga di codice successiva, utilizzare la funzione `wait()`.

**Le funzioni** sono blocchi di codice pre-programmati. Invece di dover digitare di nuovo tutto quel codice, i programmatori creano funzioni da usare come scorciatoie. Ai programmatori piacciono molto le scorciatoie. *Hello World* ha utilizzato una funzione `print()`.

### Aggiungi una funzione wait ()

Aggiungi una funzione di attesa per fare in modo che il codice attenda 3 secondi.

1. Sulla riga dopo il cambio di colore del mattone, digita `wait(3)`.

```lua
-- Changes the color of loopingPart every few seconds
local loopingPart = game.Workspace.LoopingPart
    
-- Looping Code
while true do
    loopingPart.BrickColor = BrickColor.new(0.7, 0.9, 0.9)
    -- Wait 3 seconds before next instruction
    wait(3)
end

```

{{% notice note %}}
Utilizzo di tempi di attesa diversi »
È possibile modificare il tempo di attesa purché si includa un tipo di variabile numerica tra parentesi. I tipi di variabili numeriche contengono solo numeri e non possono includere stringhe o virgolette.  
* <strong>Corretto</strong> : 5, 6.5, 22  
* <strong>Errato</strong> : cinque, "6,5", venti2
{{% /notice %}}

### Aggiunta di un secondo colore

Hai un colore, ora hai bisogno di un secondo colore per il tuo codice da alternare con il primo.

* Sotto la funzione di attesa, imposta `loopingPart.BrickColorun` ad un nuovo colore.

```lua
-- Changes the color of loopingPart every few seconds
local loopingPart = game.Workspace.LoopingPart
    
-- Looping Code
while true do
    loopingPart.BrickColor = BrickColor.new(0.7, 0.9, 0.9)
    wait(3)
    loopingPart.BrickColor = BrickColor.new(0.9, 0.4, 0.9)
end
```

* Aggiungi una seconda funzione `wait()`. Se non lo farai, il secondo colore lampeggerà così velocemente che non lo vedrai.

```lua
-- Changes the color of loopingPart every few seconds
local loopingPart = game.Workspace.LoopingPart
    
-- Looping Code
while true do
    loopingPart.BrickColor = BrickColor.new(0.7, 0.9, 0.9)
    wait(3)
    loopingPart.BrickColor = BrickColor.new(0.9, 0.4, 0.9)
    wait(3)
end
```

* Testa il tuo codice.

![loop colori](loop-colori.gif)

{{% notice warning %}}
Risoluzione dei problemi relativi al codice  
<strong>Problema :</strong> i colori vengono ignorati  
* Assicurati di avere una funzione di attesa tra ogni cambio di colore, specialmente nell'ultima riga.  
* Assicurati che il codice che desideri ripetere sia compreso tra while true doe end.  
<strong>Problema :</strong> la parte è ancora grigia o non cambia colore come previsto  
* Assicurati che tutti i valori RGB abbiano numeri da 0 a 1, siano decimali e separati da virgole.
{{% /notice %}}

* Continua ad aggiungere colori e funzioni `wait()` finché non avrai tanti colori quanti ne desideri. Prova diversi valori RGB e tempi per le funzioni di attesa.

### Esempio di codice finito

```lua
-- Changes the color of loopingPart every few seconds
-- Create a variable to store the part
local loopingPart = game.Workspace.LoopingPart

-- Looping Code
while true do
    -- Changes loopingPart's color
    loopingPart.BrickColor = BrickColor.new(0.7, 0.9, 0.9)
    -- Wait 3 seconds before next instruction
    wait(3)
    loopingPart.BrickColor = BrickColor.new(0.9, 0.4, 0.9)
    wait(3)
    loopingPart.BrickColor = BrickColor.new(0.4, 0.5, 0.4)
    wait(3)
end

```