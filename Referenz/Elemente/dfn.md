[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<dfn>

Das `<dfn>`-Element wird für die Hervorhebung des zum ersten Mal erwähnten Begriffs verwendet. Im Browser wird der Inhalt des Elements durch die Kursivschrift hervorgehoben.

Das Vorgänger Element, wie zum Beispiel ein `<p>`-Element, eine `<dt>`/`<dd>`-Paarung oder der nächstgelegene Abschnittsvorgänger des `<dfn>`-Elements wird als Definition des Begriffs betrachtet.

Der Begriff innerhalb des `<dfn>`-Elements kann einer der folgenden sein:

1. Genau wie der Inhalt des `<dfn>`-Elements:

```html
<p><dfn>HTML</dfn> ist die Standardauszeichnungssprache für die Erstellung von Webseiten.</p>
```

2. Mit dem zusätzlichen globalen `title`-Attribut. Der Wert des Attributs wird als Begriff, der definiert sein soll, betrachtet:

```html
<p><dfn title="Hypertext Markup Language">HTML</dfn> ist die Standardauszeichnungssprache für die Erstellung von Webseiten.</p>
```

3. Mit einem `<abbr>`-Element innerhalb des `<dfn>`-Elements:

```html
<p><dfn><abbr title="HyperText Markup Language">HTML</abbr></dfn> ist die Standardauszeichnungssprache für die Erstellung von Webseiten.</p>
```

4. Oder mit einem zusätzlichen globalen `id`-Attribut. Dann kann bei jeder Verwendung eines Begriffs mit einem `<a>`-Element auf die Definition verwiesen werden:

```html
<p>Lerne <a href="#html">HTML</a>.</p>
<p><dfn id="html">HTML</dfn> ist die Standardauszeichnungssprache für die Erstellung von Webseiten.</p>
```

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).
