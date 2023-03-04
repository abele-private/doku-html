[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<col>

Das `<col>`-Element ist nützlich, um Stile auf ganze Spalten anzuwenden, anstatt die Stile für jede Zelle und jede Zeile zu wiederholen. Es befindet sich in der Regel innerhalb eines `<colgroup>`-Elements.

```html
<table>
    <caption>Tabellenüberschrift</caption>
    <colgroup>
        <col>
        <col style="background-color: red">
        <col style="background-color: yellow">
    </colgroup>
    
    <thead>
    ...
</table>
```

Das Element wird innerhalb des `<table>`-Elements, vor `<thead>`, `<tbody>`, `<tfoot>` oder `<tr> und nach `<caption>` platziert.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### span

Das `span`-Attribut definiert die Anzahl der Spalten, die ein `<col>`-Element umspannen soll. Der Wert muss eine positive Ganzzahl sein. Wenn keine Zahl eingegeben ist, wird der Wert automatisch `1` betragen.

```html
<col span="2" style="background-color: green">
```

## Veraltete Attribute

### align

Das `align`-Attribut gibt an, wie die horizontale Ausrichtung des Inhalts jeder Spaltenzelle gehandhabt werden soll.

```html
<col align="center">
```

| Wert | Beschreibung |
| ---- | ------------ |
| left | Ausrichtung des Inhalts am linken Rand der Zelle |
| center | Zentrierung des Inhalts in der Zelle |
| right | Ausrichtung des Inhalts am rechten Rand der Zelle |
| justify | Ausrichtung des Inhalts als Blocksatz, so dass der Inhalt in der Zelle ausgerichtet wird |
| char | Ausrichtung des Inhalts an einem Zeichen, dass im `char`-Attribute definiert wurde |

Wenn dieses Attribut nicht gesetzt ist, wird sein Wert von der Ausrichtung des `<colgroup>`-Elements übernommen, zu dem dieses `<col>`-Element gehört. Wenn es keine gibt, wird der Wert `left` übernommen.

Um die gleiche Wirkung wie mit den Werten `left`, `center`, `right` oder `justify` zu erzielen, sollte man nicht versuchen, die CSS-Eigenschaft `text-align` auf einen Selektor zu setzen, der ein `<col>`-Element ergibt. Da `<td>`-Elemente nicht von dem `<col>`-Element abstammen, erben sie diese Eigenschaft nicht.

Wenn die Tabelle kein `colspan`-Attribut verwendet, kann man den CSS-Selektor `td:nth-child(n)` verwenden. `n` ist die Position der Spalte in der Tabelle, zum Beispiel `td:nth-child(2) { text-align: right; }`, um die zweite Spalte rechts auszurichten.

### bgcolor

Das `bgcolor`-Attribut definiert die Hintergrundfarbe der Zellen (hexadezimalen RGB-Code oder Farbschlüsselwörter). Um einen ähnlichen Effekt zu erzielen, kann man die CSS-Eigenschaft `background-color`verwenden.

```html
<col bgcolor="#FF0000">
```

### char

Das `char`-Attribut wird verwendet, um das Zeichen festzulegen, an dem die Zellen in einer Spalte ausgerichtet werden sollen. Typische Werte hierfür sind ein Punkt (.), wenn Zahlen oder Geldwerte ausgerichtet werden sollen. Wenn `align` nicht auf `char` gesetzt ist, wird dieses Attribut ignoriert.

```html
<col align="char" char=",">
```

### charoff

Das `charoff`-Attribut wird verwendet, um die Anzahl (Ganzzahl) der Zeichen anzugeben, um die Spaltendaten von den durch das `char`-Attribut spezifizierten Ausrichtungszeichen zu versetzen. Ein positiver Wert verschiebt den Inhalt nach rechts, ein negatives nach links.

```html
<col align="char" char="," charoff="2">
```

### valign

Das `valign`-Attribut legt die vertikale Ausrichtung des Textes in jeder Zelle der Spalte fest.

```html
<col valign="middle">
```

| Wert | Beschreibung |
| ---- | ------------ |
| baseline | Der Text wird so nah wie möglich am unteren Rand der Zelle platziert, aber an der Grundlinie der Zeichen und nicht am unteren Rand der Zeichen ausgerichtet. Wenn alle Zeichen die gleiche Größe haben, hat dies die gleiche Wirkung wie `bottom`. |
| bottom | Der Text wird so nah wie möglich am unteren Rand der Zelle platziert. |
| middle | Der Text wird in der Zelle zentriert. |
| top | Der Text wird so nah wie möglich an den oberen Rand der Zelle gesetzt. |

Wenn die Tabelle kein `colspan`-Attribut verwendet, kann man den CSS-Selektor `td:nth-child(n)` verwenden. `n` ist die Position der Spalte in der Tabelle, zum Beispiel `td:nth-child(2) { vertical-align: middle; }`, um die zweite Spalte rechts auszurichten.

### width

Das `width`-Attribut legt eine Standardbreite für jede Spalte in der aktuellen Spaltengruppe fest. Zusätzlich zu den Standard-Pixel- und Prozentwerten kann dieses Attribut die spezielle Form `n*` annehmen, was bedeutet, dass die Breite jeder Spalte in der Gruppe die Mindestbreite sein sollte, die notwendig ist, um den Inhalt der Spalte aufzunehmen.

```html
<col width="10*">
```
