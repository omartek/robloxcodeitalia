---
title: Riutilizzo del codice
weight: 55
tags: ["coding base"] 
---

## Riutilizzo del codice con script.Parent

Il codice che hai utilizzato finora non verrà eseguito se sono presenti più parti con lo stesso nome. Ciò significa che se desideri che più parti cambino colore, devi creare nuove parti, ognuna con nome diverso e nuovi script per ciascuna di esse. Potrebbe volerci un'eternità.

Invece di procedere in questo modo, puoi apportare una piccola modifica al codice che ti consentirà di copiarlo e incollarlo in qualsiasi parte.

![loop colori](cambio-colori.gif)

### Allega uno script a una parte

Invece di creare uno script in ServerScriptService, creerai un nuovo script allegandolo a una parte.

1. Crea una nuova parte e rinominala. Questa lezione utilizzerà *ColorPart*.
1. Fai clic con il pulsante destro del mouse sulla parte e selezionare **Inserisci oggetto > Nuovo script**.
1. Rinomina lo script. Questa lezione utilizzerà *ColorChangeScript*.
1. Nell'editor di script, elimina `print("Hello world!")`.
1. Copia e incolla il codice sottostante in *ColorChangeScript*. Questo crea una parte che scorre attraverso una serie di colori ogni tre secondi.

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

## Rendere riutilizzabile lo script

Con lo script corrente, è possibile modificare solo il colore di una singola parte che si chiami *LoopingPart* . Per cambiare il colore di qualsiasi parte, usa `script.Parent`. Questo comando memorizza qualunque cosa a cui l'oggetto script sia collegato. In questo caso, l'attuale script è collegato a una parte.

* Sostituisci `local loopingPart = game.Workspace.LoopingPart` come qui sotto indicato:  
`local loopingPart = script.Parent`

```lua
-- Changes the color of loopingPart every few seconds
    
-- Create a variable to store the part
local loopingPart = script.Parent
    
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

## Genitori e figli

Un **genitore** (o parent) è tutto ciò che ha oggetti, come script o parti, allegati sotto ad esso. Qualunque cosa sotto il genitore sono i suoi **figli** (o children). Nell'esempio mostrato di seguito, *ColorPart* è il genitore e *ColorChangeScript* è il figlio.

![parent e children](ColorPart_explorer.png)

Con lo script e la parte appena creati, la parte è il genitore e lo script è il figlio. Questa speciale riga di codice dirà allo script di trovare il suo genitore, la parte. Usando questa riga di codice, non devi nemmeno sapere come si chiama la parte.

## Duplica e prova parti

Ora che la variabile farà riferimento alla parte a cui è collegato lo script, puoi fare tutte le copie che desideri.

1. Seleziona *ColorPart* nel tuo gioco.
1. Fai clic con il pulsante destro del mouse sulla parte e selezionare Copia, quindi fai nuovamente clic con il pulsante destro del mouse e selezionare Incolla. Dovresti ritrovarti con un duplicato esatto sia della parte che del copione ad essa allegato.
1. Esegui il gioco per vedere le parti in loop in azione!

![loop colori](cambio-colori.gif)