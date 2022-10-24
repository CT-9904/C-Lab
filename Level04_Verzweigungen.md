# Verzweigungen

Bei Verzweigungen handelt es sich um eine Form von Kontrollstrukturen in Programmiersprachen. Verzweigungen werden genutzt um den Programmablauf so zu steuern, dass es je
nach Input, ein anderes Verhalten hat. Eines der gängigsten Fälle sind User-Eingaben. So gut wie jedes Programm und jede App sind so aufgebaut, dass sie dem User die
Möglichkeit bieten zu entscheiden, welchen Output er von der jeweiligen Anwendung haben möchte.

Es gibt zwei Arten von Verzweigungen. Zum einen gibt es die if-else-Verzweigung und zum Anderen die switch-case-Verzweigung.

## Die if-else-Verzweigung

Die if-else-Verzweigung ist wohl die Bekanntere von den Beiden. Diese Verzweigungsart besteht aus drei Komponenten, nämlich dem if-Block, einem oder mehreren
else if-Blöcken und einem else-Block. Je nach dem was für eine Verzweigung man aufbaut, kann man die Blöcke unterschiedlich variieren. Allerdings gelten zwei Grundregeln:

1. In einer Verzweigung, dieser Art, muss der if-Block einmal vorkommen und ganz oben stehen. Der if-Block leitet also die if-else-Verzweigung ein.

2. else if-Blöcke und der else-Block können, müssen jedoch nicht benutzt werden. Ihre Anwendung in der Anwendung ist also optional. Man darf beliebig viele else if-Blöcke
verwenden, wie man möchte. Sie müssen nur alle unter der dem if-Block stehen. Der else-Block darf, wenn er benutzt wird, nur einmal vorkommen. Er muss unter dem if-Block
bzw. nach dem letzten else if-Block stehen.

### Aufbau der einzelnen Blöcke

Aufbau des if-Blocks:

Der if-Block besteht aus drei Komponenten: dem Schlüsselwort if, einem runden Klammernpaar für, eine oder mehrere, Bedingungen und einem Anweisungsblock.
<details>
  
```c
if (Bedingungen)
{

  Anweisungen
  
}
```

</details>

Aufbau des else if-Blocks:

Der einzige Unterschied, zwischen dem if-Block und dem else if-Block, ist das Schlüsselwort vor den runden Klammern für die Bedingungen. Ansonsten ist ihr Aufbau
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

Der else-Block besteht nur aus dem Schlüsselwort und dem Anweisungsblock. Der else-Block steht immer ganz am Ende und deckt alle Fälle ab, die keine konkrete
Bedingungen haben müssen.
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
  
  int main(){
  int Antwort =0 ;
  
  printf("Was ist 1 + 1?\n");
  printf("Antwort: ");
  scanf("%d", &Antwort);
  
  if(Antwort == 2){
  printf("Die eingebene Antwort ist richtig!");
  }
  else{
  printf("Die eingebene Antwort ist falsch.");
  }
  
  return 0;
  }
  ```
</details>

<details>
<summary>Beschreibung</summary>

An diesem einfachen Beispiel sieht man den grundlegenden Ablauf einer if-else-Verzweigung. Im Beispiel wird vom User erfragt, was die Antwort auf die Rechenaufgabe
1 + 1 ist. Gibt der User die richtige Antwort (in diesem Fall eine 2) ein, so erhält er die vom Programm die Bestätigung, dass siene Antwort richtig ist. Bei einer falschen Antwort, wird man darauf hingewiesen, das die Eingabe falsch war.
  

  
</details>

  
## Die switch-case-Verzweigung

Will man Fallunterscheidungen durchführen sind switch-case-Anweisungen die geeignetere Wahl, als die if-else-Verzweigungen. Eine switch-case-Verzweigung besteht
aus drei Komponenten. Den Rahmen einer solchen Verzweigung bildet der switch-Block. In ihm erhalten sind zum einen case-Blöcke sowie max. ein default-Block.

Die case-Blöcke sind die if-, else-if-Blöcke der switch-case-Verzweigung. Der default-Block ist das Pedant zum else-Block und genau wie dieser darf er nur einmal
in der Verzeigung vorkommen und muss zwingend nach dem letzten case-Block stehen.

<details>
<summary>Hinweis</summary>
  
  Für Fallunterscheidungen sollte man die switch-case-Verzweigung vorziehen. Will man Werte miteinander vergleichen ist die if-else-Verzweigung die geeignetere Wahl.
</details>
 
### Aufbau der einzelnen Blöcke
 
Aufbau des switch-Blocks:
 
Der Aufbau des switch-Blocks ähnelt sehr dem eines if-Blocks. Er besteht aus einem Schlüsselwort, einem runden Klammernpaar dahinter und einem Anweisungsblock.
Das Schlüsselwort, dass die Verzweigung einleitet, lautet switch. In dem runden Klammernpaar stehen hier nicht Bedingungen, sondern ein Ausdruck der mit den
verschiedenen Fällen verglichen wird. Der Anweisungsblock enthält keine Anweisungen die ausgeführt werden sollen, sondern die case-Blöcke und den default-Block.
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

Der case-Block wird mit dem Schlüsselwort case eingeleitet. Auf das Schlüsselwort folgt ein Wert, der mit dem Ausdruck in Klammern des switch-Blocks, verglichen wird.
Die Syntax gibt vor, das hinter dem Wert ein Doppelpunkt (:) stehen muss. Auf deiesen Dopplepunkt folgt der Anweisungsblock. Hier stehen die Anweisungen, die beim
eintreffen des Falles, ausgeführt werden sollen.

<details>
  
  ```c
  case Konst. : {Anweisungen}
  ```
  
</details>

Im Anweisungsblock jedes case-Blocks muss nach der letzten Anweisung der Befehl break stehen. Dieser Befehl sorgt dafür, dass die Verzweigung, ab diesem Punkt,
verlassen wird. lässt man einen Befehl weg, wird die Verzweigung solange weiter ausgeführt, bis das Programm wieder auf einen break-Befehl innerhalb der Verzweigung
trifft. Lässt man sämtliche break-Befehle weg, so wird ab dem Moment, wo der Ausdruck des switch-Blocks mit einem Fall übereinstimmt, alle Anweisungen innerhalb
der Verzweigung ausgeführt.

<details>
<summary>Hinweis</summary>
Sowohl der Ausdruck im switch-Block, als auch der Wert des case-Blocks, müssen konstante Ganzzahlen sein.
</details>

Aufbau des default-Blocks:
Der default-Block wird mit dem Schlüsselwort eingeleitet. Wie auch der else-Block keine Bedingungen hat, hat auch der default-Block keinen Wert, der mit dem Ausdruck
aus dem switch-Block verglichen werden kann. Auf das Schlüsselwort der Doppelpunkt. Dahinter kommt der Anweisungsblock.

<details>
  
  ```c
  default: {Anweisungen}
  ```
  
</details>
 
