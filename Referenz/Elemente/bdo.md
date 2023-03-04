[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<bdo>

Das `<bdo>`-Element setzt die aktuelle Schreibrichtung des Textes außer Kraft, so dass der darin enthaltene Text in einer anderen Richtung wiedergegeben wird.

```html
<p>Sein Name ist <bdo dir="rtl">أحمد</bdo>.</p>
```

BDO steht für Bi-Directional Override (Bidirektionales Überschreiben).

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### dir

Das `dir`-Attribut ist obligatorische, es bestimmt die Richtung innerhalb des Elements.

| Wert | Beschreibung |
| ---- | ------------ |
| ltr | Richtung des Textes von links nach rechts. |
| rtl | Richtung des Textes von rechts nach links. |

Die Zeichen des Textes werden vom Startpunkt aus in die angegebene Richtung angezeigt; die Ausrichtung der einzelnen Zeichen wird nicht beeinflusst (so werden zum Beispiel die Zeichen nicht rückwärts ausgegeben).
