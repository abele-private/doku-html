[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<data>

Das `data`-Element wird verwendet, um eine maschinenlesbare Übersetzung eines bestimmten Inhalts hinzuzufügen.

```html
<ul>
  <li><data value="21053">Kartoffeln</data></li>
  <li><data value="21054">Zwiebeln</data></li>
  <li><data value="21055">Tomaten</data></li>
</ul>
```

Dieses Element liefert sowohl einen maschinenlesbaren Wert für Datenverarbeiter als auch einen menschenlesbaren Wert für die Darstellung in einem Browser. Wenn der Inhalt zeit- oder datumsbezogen ist, verwenden man stattdessen das `<time>`-Element.

Das Element kann in den Fällen nützlich sein, wenn die Daten in einem bestimmten Format vorliegen sollen, das für die Ausführung von Skripten erforderlich ist, aber man nicht möchte, dass Benutzer dieses Format sehen. Man möchte beispielsweise eine Liste der Produkte anzeigen, aus der Benutzer auswählen können. Jedes Produkt hat seine ID, aber man möchte diese Informationen nicht den Benutzern zeigen. Dann platziert man die Produkt-IDs im `<data>`-Element und das Gerät verarbeitet diese Informationen und zeigt dem Benutzer das Produkt mit der entsprechenden ID.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### value

Das `value`-Attribut gibt die maschinenlesbare Übersetzung des Inhalts des Elements an.

```html
<data value="5">Tomaten</data>
```
