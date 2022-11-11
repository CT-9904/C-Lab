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
