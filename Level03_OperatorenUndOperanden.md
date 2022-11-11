# Operatoren und Operanden

<details>
<summary>Operatoren</summary>

In C erfolgt die Programmausführung mittels Operatoren. Operatoren werden dazu genutzt, die Bestandteile ein einem Programmcode miteinander zu verknüpfen. Am Bekanntesten ist der Zuweisungsoperator (=). Darüber hinaus gibt es noch die Arithmetischen, Logischen, Bit-Operatoren, sowie die Vergleichsoperatoren.

</details>

<details>
<summary>Operanden</summary>

Als Operanden werden die Einheiten bezeichnet, die durch Operatoren bearbeitet (ausgelesen oder verändert) werden. Operanden sind nichts anderes als Variablen und Konstanten.

DIe Verkettung von Operanden und Operatoren bezeichnet man als Ausdruck. Jeder Ausdruck generiert einen Rückgabewert, der an den Aufruf zurückgegeben wird.

</details>

## Der Zuweisungsoprator

Wie schon erwähnt, ist der Zuweisungsoperator der Bekannteste. Mit dem Zuweisungsoperator werden Variablen Werte zugewiesen. Wie auch im normalen Sprachgebrauch steht links vom = die Variable (der Variablenname) und rechts davon der Wert.

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int x = 5; // Variable x wird der Wert 5 zugewiesen

    return 0;
}
```

</details>

## Die arithmetischen Operatoren

Die arithmetischen Operatoren sind aus der Mathematik bekannt.Es handelt sich um Plus (+), Minus (-), Mal (*), Geteilt (/) und Modulo (%).

Mit Ausnahme des Modulo-Operators, dürfen die arithmetischen Operatoren sowohl bei Ganzzahligen als auch bei Gleitkommatypen benutzt werden. Modulo hingegen darf nur bei ganzzahligen Typen verwendet werden.

Wie  auch in Mathe gilt die Punkt-vor-Strich-Regel, wenn man mehrere Operatoren gleichzeitig verwendet. Will man dies vermeiden, sollte man Klammern (()) verwenden. Der Klammer-Operator ist der Operator mit der höchsten Priorität.

<details>
<summary>Bedeutung von Modulo</summary>

Mit dem Modulo-Operator wird eine Division durchgeführt. Allerdings wird nicht das exakte Ergebnis ausgegeben, sondern der Rest der beim Dividieren entsteht.

Bei 12 % 2 ist das Ergebnis 0, da bei der Division kein Rest entsteht.

Bei 13 % 2 ist das Ergebnis 1.

</details>

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int Zahl1 = 64;
    int Zahl2 = 8;

    int Ergebnis;

    //Addition - Anwendung vom Plus-Operator
    Ergebnis = Zahl1 + Zahl2;
    printf("%d + %d = %d\n", Zahl1, Zahl2, Ergebnis);

    //Subtraktion - Anwendung vom Minus-Operator
    Ergebnis = Zahl1 - Zahl2;
    printf("%d - %d = %d\n", Zahl1, Zahl2, Ergebnis);

    //Multiplikation - Anwendung vom Mal-Operator
    Ergebnis = Zahl1 * Zahl2;
    printf("%d * %d = %d\n", Zahl1, Zahl2, Ergebnis);

    //Division - Anwendung vom Geteilt-Operator
    Ergebnis = Zahl1 / Zahl2;
    printf("%d / %d = %d\n", Zahl1, Zahl2, Ergebnis);

    //Modulodivision - Anwendung vom Modulo-Operator
    Ergebnis = Zahl1 % Zahl2;
    printf("%d %% %d = %d\n", Zahl1, Zahl2, Ergebnis);

    return 0;
}
```

</details>

## Inkrementieren und Dekrementieren

Wenn man einen Wert um eins erhöhen oder verringern möchte, bietet sich eine Inkrementierung (Erhöhung um eins) bzw.eine Dekrementierung (Verringerung um eins) an. Sowohl der Inkrement-Operator (++) als auch der Dekrement-Operator (--) können sowohl vor, als auch naach einer Variable stehen. Man spricht dann Postfix bzw. Präfix.

Bedeutung Inkrement-Operator:

```c
Variable++;
// hat die gleiche Bedeutung wie:
Variable = Variable + 1; 
```

Bedeutung Dekrement-Operator:

```c
Variable--;
// hat die gleiche Bedeutung wie:
Variable = Variable - 1;
```

<details>
<summary>Bedeutung Postfix</summary>

Bei der Postfix-Schreibweise wird die Variable nach ihrer Verwendung inkrementiert bzw. dekrementiert.

Schreibweise: Variable++ bzw. Variable--

</details>

<details>
<summary>Bedeutung Präfix</summary>

Bei der Präfix-Schreibweise wird die Variable vor ihrer Verwendung inkrementiert bzw. dekrementiert.

Schreibweise: ++Variable bzw. --Variable

</details>

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int ival = 1;

    printf("ival : %d\n", ival);    // Variable = 1
    ival++;                         // Variable = 1
    printf("ival : %d\n", ival);    // Variable = 2
    printf("ival : %d\n", ival++);  // Variable = 2
    printf("ival : %d\n", ival);    // Variable = 3
    printf("ival : %d\n", ++ival);  // Variable = 4

    return 0;
}
```

</details>

## Vergleichsoperatoren

Die Vergleichsoperatoren sollten ebenfalls aus der Mathematik bekannt vorkommen. Wie der Name schon aussag, dienen sie dazu Vergleiche durchzuführen. Es werden immer zwei Operanden miteinander verglichen zurückgegeben wird ein Wert des Typs int. Ist der Vergleich wahr, erhält man den Wert 1 (true)  zurück. Bei einem Vergleich der unwahr ist, erhält man den Wert 0 (false) zurück.

In der folgenden Tabelle sind alle Vergleichsoperatoren und ihre Bedeutungen zusammengefasst.

| Operator | Bedeutung | Beispiel | Rückgabewert |
|----------|-----------|----------|--------------|
| == | Gleich | x == y | 1, wenn x und y gleich sind / 0, wenn x und y ungleich sind |
| != | Ungleich | x != y | 1, wenn x und y ungleich sind / 0, wenn x und y gleich sind |
| < | Kleiner | x < y | 1, wenn x kleiner y ist. Ansonsten 0 |
| > | Größer | x > y | 1, wenn x größer y. Ansonsten 0 |
| <= | Kleiner gleich | x <= y | 1, wenn x kleiner oder gleich y ist. Ansonsten 0 |
| >= | Größer gleich | x >= y | 1, wenn x größer oder gleich y. Ansonsten 0 |

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int x = 9;
    int y = 5;

    _Bool Vergleich;

    // x ist gleich y
    Vergleich = x == y;
    printf("x == y -> %d\n", Vergleich);

    // x ist ungleich y
    Vergleich = x != y;
    printf("x != y -> %d\n", Vergleich);

    // x ist kleiner y
    Vergleich = x < y;
    printf("x < y -> %d\n", Vergleich);

    // x ist größer y
    Vergleich = x > y;
    printf("x > y -> %d\n", Vergleich);

    // x ist kleiner gleich y
    Vergleich = x <= y;
    printf("x <= y -> %d\n", Vergleich);

    // x ist größer gleich y
    Vergleich = x >= y;
    printf("x >= y -> %d\n", Vergleich);

    return 0;
}
```

</details>

## Der Fehler zwischen Vergleich und Zuweisung

Ein beliebter Fehler ist, dass man den Zuweisungsoperator (=) und den Gleich-Vergleichsoperator (==) miteinander verwechselt. Folgendes Beispiel dient dazu, um den Unterschied ganz explizit zu verdeutlichen:

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int x = 9; //x wird der Wert 9 zugewiesen
    int y = 5; //y wird der Wert 5 zugewiesen

    _Bool Vergleich;
    Vergleich = (x == y);
    /*
    Innerhalb der Klammer findet ein Vergleich zwischen den Variablen
    x und y, mittels dem Gleich-Vergleichsoperator statt. Das Ergebnis
    aus diesem Vergleich wird der Variablen Vergleich zugewiesen.
    */

    return 0;
}
```

## Mathematische Operationen

Mit den bisherigen Operatoren lassen sich einfache Berechnungen realisieren. Will man bestimmte mathematische Berechnungen, wie z.B. Wurzel ziehen, Trigonometrie oder Berechnungen mit komplexen Zahlen durchführen, so ist das einbinden vo zusätzlichen Headerdateien erforderlich, nämlich math.h und complex.h.

Alternativ kann man auch die Headerdatei tgmath.h benutzen. In tgmath.h sind die beiden Headerdateien math.h und complex.h enthalten. Hinzukommt das die Makros in ihr typengenerisch definiert sind.

<details>
<summary>Bedeutung von typengenerisch</summary>

Typengenerisch bedeutet, dass etwas nicht ans Typ-System gebunden ist. Konkret auf den Fall der Makros aus "tgmath.h" bezogen, bedeutet das, das man sie mit Variablen der Typen char, short, int, long, float und double nutzen kann.

</details>

## Logische Operatoren

Bei den logischen Operatoren handelt es sich um die UND- und ODER-Verknüpfung, sowie die Negation. Diese sollten aus den Grundlagen der Informatik bekannt sein.

In den folgenden Tabelle sind die logischen Operatoren, sowie deren Bedeutungen, zusammengefasst.

| Operator | Bedeutung | Beispiel |
|----------|-----------|----------|
| && | logisches UND | x && y |
| \|\| | logisches ODER | x \|\| y |
| ! | logisches NICHT | !x |

Bei logischen Operatoren gilt, dass jeder von 0 verschiedene Wert als "wahr" gewertet und 0 als "falsch" gewertet wird.

<details>
<summary>Hinweis<summary>

Bei den Verknüpfungen gilt die boolsche Algebra!

</details>

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int x = 9; // x wird der Wert 9 zugewiesen
    int y = 5; // y wird der Wert 5 zugewiesen

    int BoolWert = x && y;

    if (BoolWert > 0)
    {
        printf("x und y sind groesser 0\n");
    }
    else
    {
        printf("Mindestens ein Wert ist gleich 0\n");
    }

    y = 0;
    BoolWert = x || y;

    if (BoolWert > 0)
    {
        printf("Mindestens ein Wert ist grosser 0\n");
    }
    else
    {
        printf("Beide Werte sind 0\n");
    }

    x = !x;
    y = !y;

    printf("Wert von x: %d\n", x);
    printf("Wert von y: %d\n", y);

    return 0;
}
```

Auf die if-else-Struktur wird später konkreter eingegangen! Sie war für dieses Beispiel notwendig, um die Funktionsweise der logischen Operatoren zu verdeutlichen.

</details>

## Bit-Operatoren

Bei den Bit-Operatoren handelt es sich, unter anderem auch, um die UND- und ODER-Verknüpfung. Darüber hinaus gibt es noch die Exclusiv ODER-Verknüpfung, das Einerkomplement und die Möglichkeit Bits zu schieben. Auch hier gilt die boolsche Algebra.

Bit-Operatoren sind nur auf ganzzahlige Typen anwendbar!

Im Gegensatz zu logischen Operatoren verknüpfen Bit-Operatoren die Werte nicht in der Form, wie sie übergeben wurden, sondern bitweise.

Eine UND-Verknüpfung aus 5 und 7 also nicht "wahr" als Ergebnis, sondern sieht wie folgt aus:

| Dezimal | Binär |
|---------|-------|
| 5 | 0101 |
| 7 | 0111 |

```
        0101
UND     0111
------------
        0101 -> 5 (dezimal)
```

Zusammenfassung der Bit-Operatoren:

| Operator | Bedeutung | Erläuterung |
|----------|-----------|-------------|
| & | bitweise UND | UND-Verknüpfung von zwei Operanden |
| \| | bitweise ODER | ODER-Verknüpfung von zwei Operanden |
| ^ | bitweise Exclusiv ODER | XOR-Verknüpfung von zwei Operanden |
| ~ | Einerkomplement | Invertiert alle Bits des Operanden |
| << | Links-Shift | Niederwedertige Bits werden mit Nullen aufgefüllt |
| >> | Rechts-Shift | Höherwertige Bits werden mit Nullen aufgefüllt |

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int x = 10; // x wird der Wert 10 zugewiesen
    int y = 6;  // y wird der Wert 6 zugewiesen

    int z;

    // Bitweises UND
    z = x & y;
    printf("z: %d\n", z);

    // Bitweises ODER
    z = x | y;
    printf("z: %d\n", z);

    // Bitweises XOR
    z = x ^ y;
    printf("z: %d\n", z);

    // Shift
    z = x << 1; // Links-Shift um 1 Bit
    printf("z: %d\n", z);

    z = y >> 1; // Rechts-Shift um 1 Bit
    printf("z: %d\n", z);

    // Einerkomplement
    x = ~x;
    y = ~y;

    printf("x: %d\n", x);
    printf("y: %d\n", y);

    return 0;
}
```

</details>

## Eingabe mittels scanf-Funktion

scanf steht für "scan formatted" und bildet das Gegenstück zur Funktion printf. Mit der scanf-Funktion werden Werte, über die Standardeingabe, ins Programm eingelesen.

Auch scanf ist in der Headerdatei stdio.h deklariert.

-   -   -
Zelle1  Zelle2  Zelle3
Zelle4  Zelle5  Zelle6
-   -   -
