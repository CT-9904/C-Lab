# Datentypen

Datentypen sind für das Erstellen von Variablen und Funktionen von nöten. Bei Variablen geben sie die Speichergröße vor und wie das Bitmuster, das in der Variable gespeichert ist, zu interpretieren ist. Bei Funktionen gibt der Datentyp vor, wie der return-Wert der Funktion, zu interpretieren ist.

Es gibt zwei Arten von Datentypen, nämlich vordefinierte und abgeleitete Datentypen. Bei den vordefinierten Datentypen handelt es sich um die elementaren Typen, sowie dem Typ void. Abgeleitete Datentypen sind z.B. Pointer und Strukturen.

Auf den Typ void, sowie die abgeleiteten Datentypen, wird zu späteren Zeitpunkten konkreter drauf eingegangen. Folgend werden die elementaren Datentypen genauer erklärt.

## Elementare Datentypen

Elementare Datentypen sind nichts anderes als die ganzzahligen Typen und Gleitkommatypen.

### Ganzzahlige Typen

Bei den ganzzahligen Typen (Integer Types) handelt es sich um die Typen char, short, int und long. Die einzelnen Typen unterscheiden sich in ihrer Speichergröße und somit dem Wertebereich, den sie abspeichern können.

Besonderes gilt beim Typ char. Dieser kann genutzt werden, um Zahlen in Variablen zu speichern. Allerdings ist char der einzige Datentyp, der in der Lage ist, Zeichen abzuspeichern. char steht für "character".

Der gängiste Typ, um Ganzzahlen abzuspeichern, ist int. int steht für Integer. Man findet diesen Typ in so gut wie jeder Programmiersprache wieder.

### unsigned Typen

Bei den ganzahligen Typen gibt es die "Besonderheit", dass man sie auch unsigned (nicht vorzeichenbehaftet) nutzen kann. In unsigned Typen lassen sich immer nur positive Zahlen abspeichern. unsigned verschiebt den Wertebereich eines Typs ins Positive.

### Gleitkommatypen

Bei den Gleitkomma- oder auch Gleitpunkttypen (Floating Types) handelt es sich um die Typen float und double. Auch hier unterscheiden sich die Typen nur in der Speichergröße und den Wertebereichen, die sie abbilden können. Der Typ double ist doppelt so groß, wie ein float.

Beim schreiben eines Codes muss man darauf achten, das man Kommazahlen mit einem Punkt, statt mit einem Komma, schreibt. Das liegt einfach daran, dass die Programmiersprachen aus dem englischsprachigen Raum stammen und man dort Kommazahlen mit einem Punkt schreibt. Deswegen spricht man auch von "floating point numbers".

<details>
<summary>Hinweis</summary>

Die Speichergröße der Typen ist in C, im Vergleich zu anderen Programmiersprachen, nicht festgelegt. Sie unterscheidet je nach genutzem Compiler und der verwendeten Hardware.

</details>

### Üblicke der Datentypen

Die Daten aus den folgenden Tabellen gelten für ein 32-Bit-Sytem!

Überblick ganzzahlige Typen:

| Typ | Größe | Wertebereich | Anwendungsfall |
|-----|-------|--------------|----------------|
| char | 8 Bit / 1 Byte | -128 bis 127 | Zeichen (character) und ganze Zahlen |
| short | 16 Bit / 2 Byte | -32768 bis 32767 | ganze Zahlen |
| int | 32 Bit / 4 Byte | -2147483648 bis 2147483647 | ganze Zahlen |
| long | 32 Bit / 4 Byte | -2147483648 bis 2147483647 | ganze Zahlen |

Überblick unsigned Typen:

| Typ | Größe | Wertebereich | Anwendungsfall |
|-----|-------|--------------|----------------|
| unsigned char | 8 Bit / 1 Byte | 0 bis 255 | Zeichen (character) und ganze Zahlen |
| unsigned short | 16 Bit / 2 Byte | 0 bis 65535 | ganze Zahlen |
| unsigned int | 32 Bit / 4 Byte | 0 bis 4294967295 | ganze Zahlen |
| unsigned long | 32 Bit / 4 Byte | 0 bis 4294967295 | ganze Zahlen |

Überblick Gleitkommatypen:

| Typ | Größe | Wertebereich | Genauigkeit |
|-----|-------|--------------|-------------|
| char | 32 Bit / 4 Byte | 1,2 * 10<sup>-38</sup> bis 3,4 * 10<sup>38</sup> | 6 Nachkommastellen |
| short | 64 Bit / 8 Byte | 2,3 * 10<sup>-308</sup> bis 1,7 * 10<sup>308</sup> | 15 Nachkommastellen |
