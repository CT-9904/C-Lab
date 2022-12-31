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


