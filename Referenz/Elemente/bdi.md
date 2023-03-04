[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<bdi>

Das `<bdi>`-Element isoliert einen Teil des Textes, der möglicherweise in einer anderen Richtung formatiert ist als der übrige Text außerhalb dieses Bereichs.

```html
<p>Sein Name ist <bdi>أحمد</bdi>.</p>
```

Dieses Element ist nützlich, wenn nutzergenerierte Inhalte mit einer unbekannten Textrichtung eingebettet werden sollen. Das Element ändert nicht die Richtung des Textes, es informiert nur den Browser, den Text eventuell in einer andere Richtung zu lesen.

BDI steht für Bi-Directional Isolation (Bidirektionale Isolierung). Bidirektionaler Text ist Text, der sowohl Zeichenfolgen enthalten kann, die von links nach rechts (LTR) angeordnet sind, als auch Zeichenfolgen, die von rechts nach links (RTL) angeordnet sind, wie zum Beispiel ein arabisches Zitat, das in eine englische Zeichenfolge eingebettet ist. Browser implementieren den Unicode Bidirectional Algorithm, um dies zu handhaben. In diesem Algorithmus wird den Zeichen eine implizite Direktionalität zugewiesen: So werden beispielsweise lateinische Zeichen als LTR behandelt, während arabische Zeichen als RTL behandelt werden. Einige andere Zeichen (zum Beispiel Leerzeichen und einige Satzzeichen) werden als neutral behandelt und erhalten eine Richtungszuweisung auf der Grundlage der sie umgebenden Zeichen.

Obwohl derselbe visuelle Effekt mit der CSS-Regel `unicode-bidi: isolate;` auf einem `<span>` oder einem anderen textformatierenden Element erzielt werden kann, sollte man diesen Ansatz nicht verwenden, da er nicht semantisch ist und die Browser die CSS-Stylings ignorieren dürfen. Die Einbettung der Zeichen in `<span dir="auto">` hat denselben Effekt wie die Verwendung von `<bdi>`, aber die Semantik ist weniger klar.
