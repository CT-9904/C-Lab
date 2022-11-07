# Basics

In diesem Kapitel werden ein paar absolute Grundlagen vorgestellt, die man in der Programmiersprache C beherrschen muss! Das Kapitel soll als einfacher Einstieg in C dienen.

## Das Grundgerüst: Die main-Funktion

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    return 0;
}
```

<details>
<summary>stdio.h</summary>

Die Headerdatei stdio.h enthält alle Standardfunktionen für die Standard-Ein- und Ausgabe. Diese Headerdatei muss zwingend erhalten sein!

stdio steht für "Standard Input Output".
</details>

<details>
<summary>stdlib.h</summary>

stdlib steht für "Standard library".

Diese Headerdatei ist eine Sammlung von einer Vielzahl von Funktionen und Makros.
</details>

<details>
<summary>main-Funktion</summary>

Diese Funktion ist das Kerngerüst jedes Programms. Sie darf nur einmal enthalten sein und ohne sie ist kein Programm funktionsfähig.

Auf die Bedeutung von int wird später eingegangen.
</details>

<details>
<summary>return</summary>

Die return-Anweisung beendet die Funktion. Steht am Ende der main-Funktion "return 0;" so bedeutet das, dass das Programm ohne Fehler beendet wird.
</details>

## Die Bedeutung der geschweiften Klammern

Geschweifte Klammern ({}) bilden einen Anweisungsblock. In einem Anweisungsblock werden mehrere Anweisungen zu einer Einheit zusammengefasst. Die Anweisungen in einem Anweisungsblock werden von oben nach unten abgearbeitet.

Regel Nr.1: Geschweifte Klammern dienen dazu mehrere Anweisungen zu einem Anweisungsblock zusammenzufassen.

## Die Bedeutung des Semikolons

Das Semikolon (;) ist eines der wichtigsten Zeichen, wenn nicht sogar das wichtigste Zeichen, in C. Am Ende jeder Anweisung muss ein Semikolon stehen! Das Semikolon zeigt das Ende einer Anweisung an, genau so wie ein Punkt einen Satz beendet.

Regel Nr. 2: Jede Anweisung muss mit einem Semikolon abgeschlossen werden.

## Ausgabe mittels printf-Funktion

printf steht für "print formatted". Sie ist eine der häufig genutzen Funktionen in C. Sie gibt formattierten Text über die Standardausgabe aus. Der Text, der in die Funktion eingegeben wird, kann aus Klarschrift, Steuerzeichen und Formatzeichen bestehen.

printf ist in der Headerdatei stdio.h deklariert.

<details>
<summary>Wichtige Steuerzeichen</summary>

| Steuerzeichen | Bedeutung |
|---------------|------------------------------|
|		\0		| Null, Endzeichen für Strings |
|		\n		| Line Feed, neue Zeile		   |
|   	\f		| Form Feed, neue Seite		   |
|   	\t		| Horizontal Tab			   |
|   	\v		| Vertical Tab				   |
|   	\a		| Alert, Ton				   |
|   	\b		| Backspace, ein Zeichen zurückgehen |
|   	\'		| Ausgabe vom Zeichen: '	   |
|   	\"		| Ausgabe vom Zeichen: "	   |
|   	\?		| Ausgabe vom Zeichen: ?	   |

</details>
