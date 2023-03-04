[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<button>

Das `<button>`-Element definiert eine anklickbare Schaltfläche. Es ist ein interaktives Element, das von einem Benutzer mit einer Maus, einer Tastatur, einem Finger, einem Sprachbefehl oder einer anderen Hilfsmitteltechnologie aktiviert wird. Sobald es aktiviert ist, führt es eine Aktion aus, zum Beispiel das Absenden eines Formulars oder das Öffnen eines Dialogs.

```html
<button>
    <h6>Schaltflächer</h6>
    <p>Die Text und sonstiges enthalten kann.</p>
</button>
```

Innerhalb eines `<button>`-Elements kann man Text (und Elemente wie `<i>`, `<b>`, `<strong>`, `<br>`, `<img>`, …) einfügen. Das ist bei einer Schaltfläche, die mit dem `<input>`-Element erstellt wurde, nicht möglich. Das `type`-Attribut sollte immer für ein Schaltflächenelement angegeben werden, um den Browsern mitzuteilen, um welche Art von Schaltfläche es sich handelt.

Standardmäßig werden HTML-Schaltflächen in einem Stil dargestellt, der der Plattform ähnelt, auf der der User-Agent läuft.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### autofocus

Das `autofocus`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn es vorhanden ist, gibt es an, dass eine Schaltfläche automatisch den Fokus erhalten soll, wenn die Seite geladen wird. Nur ein Element in einem Dokument kann dieses Attribut haben.

```html
<button type="button" autofocus>Hier klicken</button>
```

### disabled

Das `disabled`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn es vorhanden ist, gibt es an, dass die Schaltfläche deaktiviert werden soll.

```html
<button type="button" disabled>Hier nicht klicken</button>
```

### form

Das `form`-Attribut gibt das Formular an, zu dem die Schaltfläche gehört. Der Wert dieses Attributs muss gleich dem `id`-Attribut eines `<form>`-Elements im selben Dokument sein. Wenn dieses Attribut nicht gesetzt ist, wird die Schaltfläche mit ihrem Vorgänger-Formular-Element verknüpft, falls vorhanden.

```html
<form action="datei.php" id="form-1"></form>

<button type="submit" form="form-1" value="Submit">Absenden</button>
```

Wenn der Button mehrere Formulare auslösen soll, müssen deren Bezeichner durch Leerzeichen getrennt werden.

```html
<form action="datei1.php" id="form-1"></form>
<form action="datei2.php" id="form-2"></form>

<button type="submit" form="form-1 form-2" value="Submit">Absenden</button>
```

### formaction

Das `formaction`-Attribut gibt an, wohin die Formulardaten gesendet werden sollen, wenn ein Formular übermittelt wird. Dieses Attribut hat Vorrang vor dem `action`-Attribut des Formulars.

```html
<form action="datei1.php" id="form"></form>

<button type="submit" form="form" formaction="datei2.php" value="Submit">Absenden</button>
```

Das Attribut wird nur für Schaltflächen mit `type="submit"` verwendet. Führt nichts aus, wenn es keinen Formulareigentümer gibt.

### formenctype

Das `formenctype`-Attribut gibt an, wie Formulardaten kodiert werden sollen, bevor sie an einen Server gesendet werden. Dieses Attribut hat Vorrang vor dem `enctype`-Attribut des Formulars.

```html
<form action="datei1.php" id="form"></form>

<button type="submit" form="form" formenctype="text/plain" value="Submit">Absenden</button>
```

Das Attribut wird nur für Schaltflächen mit `type="submit"` verwendet.

| Wert | Beschreibung |
| ---- | ------------ |
| application/x-www-form-urlencoded | der Standardwert, wenn das Attribut nicht verwendet wird |
| multipart/form-data | wird verwendet, um Eingabeelemente zu übermitteln, deren `type`-Attribute auf `file` gesetzt sind |
| text/plain | angegeben als Debugging-Hilfe; sollte nicht für echte Formularübermittlung verwendet werden |

### formmethod

Das `formmethod`-Attribut gibt an, welche HTTP-Methode beim Senden der Formulardaten verwendet werden soll. Dieses Attribut hat Vorrang vor dem `method`-Attribut des Formulars.

```html
<form action="datei1.php" id="form"></form>

<button type="submit" form="form" formmethod="post" value="Submit">Absenden</button>
```

Das Attribut wird nur für Schaltflächen mit `type="submit"` verwendet.

| Wert | Beschreibung |
| ---- | ------------ |
| post | Die Daten des Formulars werden in den _Body_ der HTTP-Anfrage aufgenommen, wenn sie an den Server gesendet werden. Dieses Attribut wird verwendet, wenn das Formular Informationen enthält, die nicht öffentlich sein sollten, wie zum Beispiel Anmeldedaten. |
| get | Die Formulardaten werden an die Aktions-URL des Formulars mit einem "?" angehängt, Werte mit einem "&" getrennt und die resultierende URL an den Server gesendet. Diese Methode wird nur verwendet, wenn das Formular keine Nebeneffekte hat, wie bei Suchformularen. |

### formnovalidate

Das `formnovalidate`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn es vorhanden ist, gibt es an, dass die Formulardaten beim Absenden nicht validiert werden sollen. Dieses Attribut hat Vorrang vor dem `novalidate`-Attribut des Formulars.

```html
<form action="datei1.php" id="form"></form>

<button type="submit" form="form" formnovalidate value="Submit">Absenden</button>
```

Das Attribut wird nur für Schaltflächen mit `type="submit"` verwendet.

### formtarget

Das `formtarget`-Attribut gibt an, wo die Antwort nach dem Absenden des Formulars angezeigt werden soll. Dieses Attribut hat Vorrang vor dem `target`-Attribut des Formulars.

```html
<form action="datei1.php" id="form"></form>

<button type="submit" form="form" formtarget="_blank" value="Submit">Absenden</button>
```

Das Attribut wird nur für Schaltflächen mit `type="submit"` verwendet.

| Wert | Beschreibung |
| ---- | ------------ |
| _blank | normalerweise wird eine neue Registerkarte geöffnet, der Benutzer kann die Browser-Einstellungen so konfigurieren, dass stattdessen ein neues Fenster geöffnet wird |
| _self | öffnet das verknüpfte Dokument in demselben Rahmen, in dem es angeklickt wurde (Standardeinstellung) |
| _parent | wird in der nächsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _top | wird in der höchsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _iFrame-Name_ | öffnet das verknüpfte Dokument in dem benannten Frame oder Iframe |

### name

Das `name`-Attribut wird verwendet, um auf Formulardaten zu verweisen, nachdem das Formular abgeschickt wurde, oder um das Element in einem JavaScript zu referenzieren.

```html
<button type="button" name="plus">+</button>
```

Mehrere Schaltflächenelemente können denselben Namen haben. So kann man mehrere Schaltflächen mit gleichem Namen benutzen, die unterschiedliche Werte übermitteln können, wenn sie in einem Formular verwendet werden.

### type

Das `type`-Attribut spezifiziert den Typ der Schaltfläche. Es sollte immer für das `button`-Element angegeben werden. Verschiedene Browser können unterschiedliche Standardtypen für das Schaltflächenelement verwenden.

```html
<button type="button">Knopf</button>
```

| Wert | Beschreibung |
| ---- | ------------ |
| button | die Schaltfläche ist eine anklickbare Schaltfläche ohne Effekt |
| submit | die Schaltfläche ist eine Submit-Schaltfläche (sendet Formulardaten) |
| reset | die Schaltfläche ist eine Reset-Schaltfläche (setzt die Formulardaten auf ihre ursprünglichen Werte zurück) |

Das `value`-Attribut legt den Wert fest, der mit dem Namen der Schaltfläche verbunden ist, wenn diese mit den Formulardaten übermittelt wird.

```html
<form action="datei1.php" id="form"></form>

<button type="submit" form="form" value="Submit">Absenden</button>
```

In einem Formular werden die Schaltfläche und ihr Wert nur übermittelt, wenn die Schaltfläche selbst zum Übermitteln des Formulars verwendet wurde.

## Veraltete Attribute

### autocomplete

Das `autocomplete`-Attribut ist nicht standardisiert und Firefox-spezifisch. Im Gegensatz zu anderen Browsern behält Firefox den dynamischen Deaktivierungsstatus einer Schaltfläche über mehrere Seitenladungen hinweg bei.

```html
<button type="submit" autocomplete="off">Absenden</button>
```

Die Einstellung `autocomplete="off"` deaktiviert diese Funktion.
