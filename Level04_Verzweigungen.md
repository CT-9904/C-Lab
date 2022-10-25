# Verzweigungen

Bei Verzweigungen handelt es sich um eine Form von Kontrollstrukturen in Programmiersprachen. Verzweigungen werden genutzt um den Programmablauf so zu steuern, dass es je
nach Input, ein anderes Verhalten hat. Eines der gängigsten F„lle sind User-Eingaben. So gut wie jedes Programm und jede App sind so aufgebaut, dass sie dem User die
M”glichkeit bieten zu entscheiden, welchen Output er von der jeweiligen Anwendung haben m”chte.

Es gibt zwei Arten von Verzweigungen. Zum einen gibt es die if-else-Verzweigung und zum Anderen die switch-case-Verzweigung.

## Die if-else-Verzweigung

Die if-else-Verzweigung ist wohl die Bekanntere von den Beiden. Diese Verzweigungsart besteht aus drei Komponenten, n„mlich dem if-Block, einem oder mehreren
else if-Bl”cken und einem else-Block. Je nach dem was fr eine Verzweigung man aufbaut, kann man die Bl”cke unterschiedlich variieren. Allerdings gelten zwei Grundregeln:

1. In einer Verzweigung, dieser Art, muss der if-Block einmal vorkommen und ganz oben stehen. Der if-Block leitet also die if-else-Verzweigung ein.

2. else if-Bl”cke und der else-Block k”nnen, mssen jedoch nicht benutzt werden. Ihre Anwendung in der Anwendung ist also optional. Man darf beliebig viele else if-Bl”cke verwenden, wie man m”chte. Sie mssen nur alle unter der dem if-Block stehen. Der else-Block darf, wenn er benutzt wird, nur einmal vorkommen. Er muss unter dem if-Block bzw. nach dem letzten else if-Block stehen.

### Aufbau der einzelnen Bl”cke

Aufbau des if-Blocks:

Der if-Block besteht aus drei Komponenten: dem Schlsselwort if, einem runden Klammernpaar fr, eine oder mehrere, Bedingungen und einem Anweisungsblock.
<details>
  
```c
if (Bedingungen)
{
  Anweisungen
  
}
```

</details>

Aufbau des else if-Blocks:

Der einzige Unterschied, zwischen dem if-Block und dem else if-Block, ist das Schlsselwort vor den runden Klammern fr die Bedingungen. Ansonsten ist ihr Aufbau
identisch.
<details>
  
```c
else if (Bedingungen)
{
  Anweisungen
  
}
```  

</details>

Aufbau des else-Block:

Der else-Block besteht nur aus dem Schlsselwort und dem Anweisungsblock. Der else-Block steht immer ganz am Ende und deckt alle F„lle ab, die keine konkrete
Bedingungen haben mssen.
<details>

```c
else
{
  
  Anweisungen
  
}
```

</details>

### Beispiel einer einfachen if-else-Struktur

<details>
<summary>Programmcode</summary>
  
```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int Antwort = 0;

    printf("Was ist 1 + 1?\n");
    printf("Antwort: ");
    scanf("%d", &Antwort);

    if (Antwort == 2)
    {
        printf("Die eingegebene Antwort ist richtig!");
    }
    else
    {
        printf("Die eingegebene Antwort ist falsch.");
    }

    return 0;
}
```

</details>

<details>
<summary>Beschreibung</summary>

An diesem einfachen Beispiel sieht man den grundlegenden Ablauf einer if-else-Verzweigung. Im Beispiel wird vom User erfragt, was die Antwort auf die Rechenaufgabe
1 + 1 ist. Gibt der User die richtige Antwort (in diesem Fall eine 2) ein, so erh„lt er die vom Programm die Best„tigung, dass siene Antwort richtig ist. Bei einer falschen Antwort, wird man darauf hingewiesen, das die Eingabe falsch war.

Das Beispiel macht auch deutlich, dass solche Strukturen einer bin„ren Logik folgen. L„sst man den else-Block n„mlich weg, wird das Programm zwar auch korrekt ausgefhrt. Allerdings bekommt der User nur eine Rckmeldung, wenn er die richtige Antwort eingegeben hat. Bei einer Eingabe die falsch ist, erh„lt er keine Auskunft darber, ob seine Antwort stimmt oder nicht.

<span style="color:red">
Deswegen gilt:
Will man bei einem bestimmten Ereignis, eine entsprechende Reaktion des Programms darauf haben, muss diese vorher im Quellcode definiert sein.
</span>

</details>

### Beispiel einer if-else if-else-Struktur

<details>
<summary>Programmcode</summary>
  
```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int Wert1 = 36;
    int Wert2 = 25;
    int Wert3 = 22;

    if ((Wert1 > Wert2) && (Wert1 > Wert3))
    {
        printf("Wert1 betraegt %d und ist der Groesste!\n", Wert1);
    }
    else if ((Wert2 > Wert1) && (Wert2 > Wert3))
    {
        printf("Wert2 betraegt %d und ist der Groesste!\n", Wert2);
    }
    else if ((Wert3 > Wert1) && (Wert3 > Wert2))
    {
        printf("Wert3 betraegt %d und ist der Groesste!\n", Wert3);
    }

    return 0;
}
```

</details>

<details>
<summary>Beschreibung</summary>

Wie man in diesem Beispiel sieht, eignen sich if-else if-else-Verzweigungen gut, um Werte miteinander zu vergleichen.

In diesem Beispiel wurden, in jedem Block, mehrere Bedingungen gestellt. Im Fall des if-Blocks luaten diese, dass der Wert1 gr”áer als Wert2 und Wert3 sein muss, damit dieser ausgefhrt wird.

Verknpft man mehrer Teilbedingungen miteinander, zu einer Gesamtbedingung, so ist es ratsam diese in Klammern zu setzen. Das macht den Code, zum Einen, leserlicher und, zum Anderen, fr andere Programmierer verst„ndlicher.

Bei der Ausfhrung gilt, wurden die Bedingungen eines Blocks erfllt, werden die Anweisungen darin ausgefhrt. Wenn die Bedingungen eines Blocks als erfllt gewertet sind, werden die anderen Bl”cke nicht mehr berckrichtsichtigt. Ihre Bedingungen werden nicht mehr berprft. Konkret auf das Beispiel bezogen heiát das, wurden beispielsweise die Bedingungen des if-Blocks als erfllt gewertet, werden die beiden darauf folgenden else-if-Bl”cke nicht mehr bercksichtigt.

</details>

## Die switch-case-Verzweigung

Will man Fallunterscheidungen durchfhren sind switch-case-Anweisungen die geeignetere Wahl, als die if-else-Verzweigungen. Eine switch-case-Verzweigung besteht
aus drei Komponenten. Den Rahmen einer solchen Verzweigung bildet der switch-Block. In ihm erhalten sind zum einen case-Bl”cke sowie max. ein default-Block.

Die case-Bl”cke sind die if-, else-if-Bl”cke der switch-case-Verzweigung. Der default-Block ist das Pedant zum else-Block und genau wie dieser darf er nur einmal
in der Verzeigung vorkommen und muss zwingend nach dem letzten case-Block stehen.

<details>
<summary>Hinweis</summary>
  
  Fr Fallunterscheidungen sollte man die switch-case-Verzweigung vorziehen. Will man Werte miteinander vergleichen ist die if-else-Verzweigung die geeignetere Wahl.
</details>

### Aufbau der einzelnen Bl”cke

Aufbau des switch-Blocks:

Der Aufbau des switch-Blocks „hnelt sehr dem eines if-Blocks. Er besteht aus einem Schlsselwort, einem runden Klammernpaar dahinter und einem Anweisungsblock.
Das Schlsselwort, dass die Verzweigung einleitet, lautet switch. In dem runden Klammernpaar stehen hier nicht Bedingungen, sondern ein Ausdruck der mit den
verschiedenen F„llen verglichen wird. Der Anweisungsblock enth„lt keine Anweisungen die ausgefhrt werden sollen, sondern die case-Bl”cke und den default-Block.
<details>
  
```c
switch (Ausdruck)
{
 
 case 1
  
   .
  
   .
  
   .
  
 case n
  
 default
  
  
}
```

</details>

Aufbau des case-Blocks:

Der case-Block wird mit dem Schlsselwort case eingeleitet. Auf das Schlsselwort folgt ein Wert, der mit dem Ausdruck in Klammern des switch-Blocks, verglichen wird.
Die Syntax gibt vor, das hinter dem Wert ein Doppelpunkt (:) stehen muss. Auf deiesen Dopplepunkt folgt der Anweisungsblock. Hier stehen die Anweisungen, die beim
eintreffen des Falles, ausgefhrt werden sollen.

<details>
  
  ```c
  case Konst. : {Anweisungen}
  ```
  
</details>

Im Anweisungsblock jedes case-Blocks muss nach der letzten Anweisung der Befehl break stehen. Dieser Befehl sorgt dafr, dass die Verzweigung, ab diesem Punkt,
verlassen wird. l„sst man einen Befehl weg, wird die Verzweigung solange weiter ausgefhrt, bis das Programm wieder auf einen break-Befehl innerhalb der Verzweigung
trifft. L„sst man s„mtliche break-Befehle weg, so wird ab dem Moment, wo der Ausdruck des switch-Blocks mit einem Fall bereinstimmt, alle Anweisungen innerhalb
der Verzweigung ausgefhrt.

<details>
<summary>Hinweis</summary>
Sowohl der Ausdruck im switch-Block, als auch der Wert des case-Blocks, mssen konstante Ganzzahlen sein.
</details>

Aufbau des default-Blocks:
Der default-Block wird mit dem Schlsselwort eingeleitet. Wie auch der else-Block keine Bedingungen hat, hat auch der default-Block keinen Wert, der mit dem Ausdruck
aus dem switch-Block verglichen werden kann. Auf das Schlsselwort der Doppelpunkt. Dahinter kommt der Anweisungsblock.

<details>
  
  ```c
  default: {Anweisungen}
  ```
  
</details>
