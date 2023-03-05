[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<dialog>

Das `<dialog>`-Element stellt ein Dialogfeld oder eine andere interaktive Komponente dar, zum Beispiel eine abschaltbare Warnmeldung, einen Inspektor oder ein Unterfenster. Es erleichtert das Erstellen von Popup-Dialogen und Modals auf einer Webseite.

<dialog>Dies ist ein Dialogfenster.</dialog>

Voreingestellt wird das Dialogfenster nicht angezeigt, es wird mithilfe des `open`-Attributs geöffnet.

## Attribute

Dieses Element unterstützt [globale Attribute](../Globale_Attribute.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

**Warnung:** Das globale Attribut `tabindex` darf nicht für das `<dialog>`-Element verwendet werden.

### open

Das `open`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn es vorhanden ist, gibt es an, dass das Dialogelement aktiv ist und dass der Benutzer mit ihm interagieren kann.

<dialog open>Dies ist ein sichtbares Dialogfenster.</dialog>

Wenn das `open`-Attribut nicht gesetzt ist, sollte der Dialog dem Benutzer nicht angezeigt werden. Es wird empfohlen, die JavaScript-Methoden `.show()` oder `.showModal()` zu verwenden, um Dialoge darzustellen, und nicht das `open`-Attribut. Wenn ein `<dialog>` mit dem `open`-Attribut geöffnet wird, ist er nicht-modal.
