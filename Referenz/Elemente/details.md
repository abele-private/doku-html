[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<details>

Das `<details>`-Tag gibt zusätzliche Details an, die der Benutzer bei Bedarf öffnen und schließen kann. Es wird häufig verwendet, um ein interaktives Widget zu erstellen, das sich auf- und zuklappen. In der Standardeinstellung ist das Widget geschlossen. Wenn es geöffnet wird, erweitert es sich und zeigt den Inhalt an.

```html
<details>
    <summary>Text zeigen</summary>
    <p>Hier ist der Text</p>
</details>
```

In der Regel wird es mit einem kleinen Dreieck dargestellt, das sich dreht (oder wendet), um den offenen/geschlossenen Status anzuzeigen, mit einer Beschriftung neben dem Dreieck. Das `<summary>`-Element erstellt eine sichtbare Überschrift und durch den Klick drauf wird der Inhalt angezeigt/ausgeblendet. Wenn es kein `<summary>` gibt, wird der Browser die Überschrift _Mehr_ voreingestellt anzeigen.

Innerhalb des Elements können alle HTML-Inhaltselemente, wie Text, Tabellen, Listen, Formulare und so weiter, eingefügt werden.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### open

Das `open`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn es gesetzt ist, gibt es an, dass die Details für den Benutzer sichtbar (offen) sein sollen. Standardmäßig ist dieses Attribut nicht vorhanden, was bedeutet, dass die Details nicht sichtbar sind.


Das Attribut muss vollständig entfernt werden, damit die Details ausgeblendet bleiben. `open="false"` macht die Details sichtbar, da das Attribut boolesch ist.
