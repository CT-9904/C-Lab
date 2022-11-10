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
