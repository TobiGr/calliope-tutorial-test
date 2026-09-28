# B8.3 Kleine Programmieraufträge

## Aufgabe 1 - Wie heißt du? 
Auf dem Calliope mini befindet sich eine LED-Matrix. Das sind die 
kleinen roten Lämpchen. Diese kann man man ganz unterschiedlich 
programmieren. Wie wäre es mit einem Namensschild, wenn man Knopf A drückt? Wählt dazu folgende Bausteine aus und verbinde sie miteinander: ``||basic:zeige Text||`` ``||input:wenn Knopf A geklickt||`` 

```blocks
input.onButtonEvent(Button.A, input.buttonEventClick(), function () {
basic.showString("Hallo!")
})
```

```ghost
basic.showString("Hallo!")
music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
input.onButtonEvent(Button.A, input.buttonEventClick(), function () {
})
input.onButtonEvent(Button.B, input.buttonEventClick(), function () {
})
for (let index = 0; index < 4; index++) {
}
basic.showNumber(input.temperature())
input.onGesture(Gesture.Shake, function () {	
})
basic.showNumber(randint(0, 10))
```

## Aufgabe 2 - Hast du Töne?
Der Calliope hat einen Lautsprecher, daher kann er auch Töne 
abspielen. Lasst den Calliope nach dem Drücken von Knopf B drei verschiedene Töne abspielen. 

```blocks
input.onButtonEvent(Button.B, input.buttonEventClick(), function () {
music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})

```

## Aufgabe 3 - Schleifen 
Immer wenn man möchte, dass der Computer etwas mehrmals hintereinander macht, braucht man Programmschleifen. 
Versucht es einmal mit eurem Programm aus Aufgabe 2. Die drei verschiedenen Noten sollen viermal hintereinander abgespielt werden. 

```blocks
input.onButtonEvent(Button.B, input.buttonEventClick(), function () {
for (let index = 0; index < 4; index++) {
}
})
```

## Aufgabe 4 - Schüttel mich! 
Statt der Knöpfe A und B kann man als Eingabe auch den Befehl „wenn geschüttelt" verwenden. Nun wollen wir programmieren, dass 
der Calliope mini die Temperatur anzeigt, wenn er geschüttelt wird. Nutze dazu folgende Bausteine:
``||basic:zeige Zahl||`` ``||input:Temperatur||``  ``||input:wenn geschüttelt||`` 

```blocks
input.onGesture(Gesture.Shake, function () {	
basic.showNumber(input.temperature())
})
```

## Aufgabe 5 - Würfel 
Nun versucht doch einmal, mit Hilfe des Calliope einen Würfel zu 
programmieren, wenn man die Knöpfe A und B gleichzeitig drückt. Die wesentlichen Bausteine dafür kennt ihr schon. Ihr 
braucht aber auch noch diesen Baustein:  
``||math:wähle eine zufällige Zahl||`` 

```blocks
input.onButtonEvent(Button.AB, input.buttonEventClick(), function () {
basic.showNumber(randint(0, 6))
})
```

