# Funktionen

Möchte man bestimmte Handlungsabfolgen (Algorithmen) mehrmals, an verschiedenen Stellen des Codes, nutzen, so bietet es sich an aus ihnen Funktionen zu erstellen.
Funktionen sind Zusammenfassungen bestimmter Handlungsabfolgen.
Die Funktion, ohne die kein C-Programm auskommt, ist die main-Funktion! Sie wird vom Betriebssystem als erstes aufgerufen und die in ihr enthaltene Handlungsabfolge, also das eigentliche Programm welches vom Programmierer geschrieben wurde, wird ausgeführt. Innerhalb der main-Funktion sind also alle Funktionen hinterlegt, die ausgeführt werden sollen.

In der Praxis kommt es, so gut wie, nie vor, dass man eine Problemstellung nur in der main-Funktion löst. Tatsächlich bricht man eine Problemstellung in viele kleine Teil-Probleme herunter und löst diese in Form von Funktionen.

Die Nutzung von Funktionen macht den Code ordentlicher und verbessert die Wartbarkeit. Im Falle eines Fehlers, einer bestimmten Handlungsabfolge, muss man den Coder nur an einer Stelle korrigieren. Hätte man die Handlungsabfolge mehrmals in der main-Funktion genutzt, statt sie in eine Funktion auszulagern, so müsste man einen Fehler, in der Handlungsabfolge, an jeder einzelnen Stelle korrigieren, wo diese genutzt wurde.

Es gibt zwei verschiedene Arten von Funktionen, nämlich welche von den bisher bekannten Datentypen und welche vom Typ void. Der Unterschied liegt in ihren Rückgaben. Im Gegensatz zu Funktionen von einem Datentyp, geben void-Funktionen nichts zurück.

## Der Datentyp void

Bei void (englisch für "Leere") handelt es sich nicht um einen echten Datentypen. Er wird anstelle eines Datentypen (char, short, int, long, float, double) verwendet um anzugeben, dass kein Wert benötigt wird oder vorhanden ist. Laut der Syntax von C ist void als Datentyp zu behandeln, jedoch darf er nur in ganz bestimmten Stellen verwendet werden, nämlich wenn man Funktionen erstellt oder mit Zeigern (Pointer) arbeitet.

Bei Funktionen wird void verwendet, um Funktionen zu erstellen die keine Werte zurückgeben oder eine Funktion keine Parameter hat.

Auf die Verwendung von void bei Zeigern wird später eingegangen.

## Der Grundaufbau einer Funktion

Eine Funktion besteht aus zwei grundlegenden Teilen, nämlich dem Funktionskopf und dem Funktionskörper. Beim Funktionskörper handelt es sich einfach nur um einen Anweisungsblock. der Funktionskopf ist etwas komplexer aufgebaut und besteht aus mehreren Teilkomponenten. Eine Funktion wird durch den Funktionskopf deklariert.

Syntax einer Funktion:

```c
<Datentyp><Funktionsname>([Parameter])
{
	Anweisungen
}
```

Der Funktionskopf besteht aus vier wesentlichen Bestandteilen nämlich aus einem Datentypen, einem Funktionsnamen, einem runden Klammernpaar einem oder mehreren Parametern innerhalb des runden Klammernpaares. Auf die geschlossene Klammer folgt der Funktionskörper.

## Rückgabe einer Funktion

Wie schon zu Beginn erwähnt gibt es zwei Arten von Funktionen. Sie unterscheiden sich in ihrem Rückgabewert. Der Datentyp einer Funktion gibt vor von welchem Datentyp die Rückgabe der Funktion ist oder kürzer: **Datentyp Funktion = Datentyp Rückgabewert**

Soll eine Funktion keinen Rückgabewert haben, nutzt man den Datentyp void.

## Parameter

Parameter sind Werte, die an die Funktion übergeben werden. Parameter sind optional, das runde Klammernpaar in dem sie stehen jedoch nicht! Bei einer Funktion, wo Parameter nicht erforderlich sind, lässt man das Klammernpaar leer oder schreibt (übergibt man der Funktion) ein void. Beides ist gleichwertig.

Die Parameter müssen nicht vom gleichen Datentyp sein, wie die Funktion. Wenn man also z.B. eine Funktion vom Typen float erstellt, können die Parameter von ihr auch vom Typen int sein. Der Wert, der von dieser Funktion zurückgeben wird, ist jedoch vom Datentyp float.


