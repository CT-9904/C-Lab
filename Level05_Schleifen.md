# Schleifen

Will man eine Reihe von Anweisungen in einem Programm mehrmals hintereinander verwenden, so verwendet man Schleifen um dies zu realisieren. Schleifen sind die zweite Form der Kontrollstrukturen.

In C gibt es drei verschiedene Schleifen: die for-Schleife, die while-Schleife und die do-while-Schleife.

Was alle drei Schleifen-Typen gemeinsam haben ist, dass sie eine Durchlauf-Bedingung besitzen. Eine Durchlauf-Bedingung ist eine Bedingung, die vor jedem neuen Schleifendurchlauf geprüft wird. Solange die Bedingung erfüllt ist, wird die Schleife wiederholt. Ist sie nicht bzw. nicht mehr erfüllt, wird die Schleife verlassen oder, unter entsprechenden Umständen, gar nicht erst ausgeführt.

## Kopfgesteuerte und fußsgesteurte Schleifen

Man unterscheidet zwischen zwei Arten von Schleifen, nämlich kopfgesteuerten und fußgesteuerten Schleifen. Der Unterschied zwischen den zwei Arten ist einfach erklärt.

Bei den kopfgesteuerten Schleifen wird die Durchlauf-Bedingung immer vor einem Durchlauf geprüft. Sie steht über dem Anweisungsblock, also am Kopf der Schleife. Diefor-Schleife und die while-Schleife sind beides kopfgesteuerte Schleifen.

Bei fußgesteuerten Schleifen wird die Durchlauf-Bedingung ganz zum Schluss geprüft (nach dem Durchlauf). Sie steht unter dem Anweisungsblock, als am Fuß der Schleife. Die do-while-Schleife ist eine fußgesteuerte Schleife.

Der Hauptunterschied zwischen den beiden Arten liegt darin, das eine fußgesteuerte Schleife IMMER einmal ausgeführt wird, bevor ihre Durchlauf-Bedingung geprüft wird. Bei einer kopfgesteuerten Schleife wird vor der Ausführung die Durchlauf-Bedingung geprüft. Es kann vorkommen, dass die Durchlauf-Bedingung bereits vor der ersten Ausführung nicht mehr erfüllt ist. In diesem Fall wird eine kopfgesteuerte Schleife garnicht erst ausgeführt.

## Die for-Schleife

Die for-Schleife ist die Schleife mit der man, in der Praxis, häufiger in Berührung kommt. Wenn die Anzahl der Iterationen (wie häufig die Schleife wiederholt werden soll) bekannt ist oder sie sogar fix sein muss, ist es gängige Praxis die for-Schleife zu nutzen. Sie ist wie folgt aufgebaut:

```c
for (Bereich 1; Bereich 2; Bereich 3){
	Anweisungen
}
```

Die Schleife wird mit dem Schlüsselwort for eingeleitet. Dahinter ist ein rundes Klammernpaar, was verschiedene Bedingungen enthält. Der Inhalt des rundes Klammernpaares ist in drei Bereiche aufgeteilt:

<details>
<summary>Bereich 1: Start-Bedingung (Initialisierung)</summary>

Die Start-Bedingung (Bereich 1) wird nur ganz am Anfang, vor dem ersten Schleifendurchlauf, geprüft. Ist sie erfüllt, wird die Schleife ausgeführt. Anderenfalls wird sie komplett übersprungen. Für die Start-Bedingung wird üblicherweise eine Zählvariable gewählt.
</details>

<details>
<summary>Bereich 2: Durchlauf-Bedingung</summary>

Die Durchlauf-Bedingung (Bereich 2) wird vor jedem Schleifendurchlauf geprüft. Die Schleife wird beendet, wenn sie nicht mehr erfüllt ist.
</details>

<details>
<summary>Bereich 3: Operation (Reinitialsierung)</summary>

Die Operation (Bereich 3) dient dazu, die Zählvaraible der Start-Bedingung zu erhöhen / verringern. Meistens wird eine Inkrementierung um den Wert 1 gewählt. Die Operation wird immer am Ende eines Schleifendurchlaufs ausgeführt.
</details>

Die einzelnen Bereiche sind jeweils durch ein Semikolon voneinander getrennt. Auf das runde Klammernpaar folgt der Anweisungsblock.

<details>
<summary>Beispiel</summary>

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int cycle = 0;

    for (int i = 0; i < 5; i++)
    {
        cycle = i + 1;
        printf("%d. Durchlauf\n", cycle);
    }

    return 0;
}
```

Das Beispiel zeigt eine for-Schleife die fünf Durchläufe ausführt und ihren aktuellen Schleifendurchlauf, mittels printf-Anweisung, auf der Konsole ausgibt.

Die Hilfsvariable cycle dient dazu die Nummer des jeweiligen Schleifendurchlaufs abzuspeichern. Sie wird außerhalb der for-Schleife mit dem Wert 0 initialisiert. Innerhalb der for-Schleife wird ihr der Wert der Variable i + 1 zugewiesen. Hätte man cycle innerhalb der for-Schleife mit dem Wert 0 initialisiert, würde bei jedem neuen Schleifendurchlauf die Initialisierung von neuem stattfinden.

Der Wert der Variable i (Variable der Start-Bedingung der for-Schleife) konnte nicht als Nummer des jeweiligen Schleifendurchlaufs verwendet werden, da sie mit dem Wert 0 initialisiert wurde. In der Informatik ist es nämlich üblich, dass man bei 0 anfängt zu zählen.
Aus diesem Grund lautet die Durchlaufbedingung auch i < 5 für fünf Schleifendurchläufe. Würde man die Durchlauf-Bedingung i <= 5 stellen, würde die Schleife insgesamt sechs Durchläufe ausführen.

<details>
<summary>Anmerkung</summary>

Im Kapitel über Arrays wird deutlich, warum es Sinn macht dass for-Schleifen von 0 aus operieren.
</details>

</details>
