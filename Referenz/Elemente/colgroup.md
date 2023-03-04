[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<colgroup>

Das `<colgroup>`-Element legt eine Gruppe von einer oder mehreren Spalten in einer Tabelle für die Formatierung fest. Es ist nützlich, um Stile auf ganze Spalten anzuwenden, anstatt die Stile für jede Zelle, für jede Zeile zu wiederholen.

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

Das `<colgroup>`-Element wird innerhalb des `<table>`-Elements, vor `<thead>`, `<tbody>`, `<tfoot>` und `<tr>`; und nach dem `<caption>`-Element platziert. Um verschiedene Eigenschaften für eine Spalte innerhalb einer `<colgroup>` zu definieren, verwendet man das `<col>`-Element innerhalb des `<colgroup>`-Elements.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### span

Das `span`-Attribut gibt die Anzahl der Spalten an, die eine Spaltengruppe umfassen soll.

<table>
    <caption>Tabellenüberschrift</caption>
    <colgroup span="2"></colgroup>
    
    <thead>
    ...
</table>
```

Der Wert muss eine positive Ganzzahl sein, die die Anzahl der aufeinanderfolgenden Spalten angibt, über die sich das `<colgroup>`-Element erstreckt. Wenn es nicht vorhanden ist, ist sein Standardwert `1`. Das `span`-Attribut ist nicht zulässig, wenn es ein oder mehrere `<col>`-Elemente innerhalb der `<colgroup>` gibt.

## Veraltete Attribute

### align

Das `align`-Attribut gibt an, wie die horizontale Ausrichtung des Inhalts jeder Spaltenzelle gehandhabt werden soll.

```html
<colgroup align="center">
```

| Wert | Beschreibung |
| ---- | ------------ |
| left | Ausrichtung des Inhalts am linken Rand der Zelle |
| center | Zentrierung des Inhalts in der Zelle |
| right | Ausrichtung des Inhalts am rechten Rand der Zelle |
| justify | Ausrichtung des Inhalts als Blocksatz, so dass der Inhalt in der Zelle ausgerichtet wird |
| char | Ausrichtung des Inhalts an einem Zeichen, dass im `char`-Attribute definiert wurde |

Um die gleiche Wirkung wie mit den Werten `left`, `center`, `right` oder `justify` zu erzielen, sollte man nicht versuchen, die CSS-Eigenschaft `text-align` auf einen Selektor zu setzen, der ein `<colgroup>`-Element ergibt. Da `<td>`-Elemente nicht von dem `<colgroup>`-Element abstammen, erben sie diese Eigenschaft nicht.

Wenn die Tabelle kein `colspan`-Attribut verwendet, kann man den CSS-Selektor `td:nth-child(n)` verwenden. `n` ist die Position der Spalte in der Tabelle, zum Beispiel `td:nth-child(2) { text-align: right; }`, um die zweite Spalte rechts auszurichten.

### bgcolor

Das `bgcolor`-Attribut definiert die Hintergrundfarbe der Zellen (hexadezimalen RGB-Code oder Farbschlüsselwörter). Um einen ähnlichen Effekt zu erzielen, kann man die CSS-Eigenschaft `background-color`verwenden.

```html
<colgroup bgcolor="#FF0000">
```

### char

Das `char`-Attribut wird verwendet, um das Zeichen festzulegen, an dem die Zellen in einer Spalte ausgerichtet werden sollen. Typische Werte hierfür sind ein Punkt (.), wenn Zahlen oder Geldwerte ausgerichtet werden sollen. Wenn `align` nicht auf `char` gesetzt ist, wird dieses Attribut ignoriert.

```html
<colgroup align="char" char=",">
```

### charoff

Das `charoff`-Attribut wird verwendet, um die Anzahl (Ganzzahl) der Zeichen anzugeben, um die Spaltendaten von den durch das `char`-Attribut spezifizierten Ausrichtungszeichen zu versetzen. Ein positiver Wert verschiebt den Inhalt nach rechts, ein negatives nach links.

```html
<colgroup align="char" char="," charoff="2">
```

### valign

Das `valign`-Attribut legt die vertikale Ausrichtung des Textes in jeder Zelle der Spalte fest.

```html
<colgroup valign="middle">
```

| Wert | Beschreibung |
| ---- | ------------ |
| baseline | Der Text wird so nah wie möglich am unteren Rand der Zelle platziert, aber an der Grundlinie der Zeichen und nicht am unteren Rand der Zeichen ausgerichtet. Wenn alle Zeichen die gleiche Größe haben, hat dies die gleiche Wirkung wie `bottom`. |
| bottom | Der Text wird so nah wie möglich am unteren Rand der Zelle platziert. |
| middle | Der Text wird in der Zelle zentriert. |
| top | Der Text wird so nah wie möglich an den oberen Rand der Zelle gesetzt. |

Wenn die Tabelle kein `colspan`-Attribut verwendet, kann man den CSS-Selektor `td:nth-child(n)` verwenden. `n` ist die Position der Spalte in der Tabelle, zum Beispiel `td:nth-child(2) { vertical-align: middle; }`, um die zweite Spalte rechts auszurichten.
