[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<dd>

Das `<dd>`-Element wird verwendet, um einen Begriff/Namen in einer Beschreibungsliste zu beschreiben. Innerhalb eines des Elements kann man Absätze, Zeilenumbrüche, Bilder, Links, Listen und so weiter einfügen.

```html
<dl>
    <dt>Kaffee</dt>
    <dd>Schwarzes Heißgetränk aus der Kaffeebohne.</dd>
    <dt>Milch</dt>
    <dd>Weißes Kaltgetränk aus dem Euter der Kuh.</dd>
</dl>
```

Das Element wird mit den Elementen `<dl>` und `<dt>` für die Beschreibung der Begriffe in der Liste von Erklärungen verwendet. Im `<dd>`-Element wird die Beschreibung des Begriffs, der durch das `<dt>`-Element definiert wird, geschrieben. Für die Bestimmung der Liste wird das `<dl>`-Element verwendet. Ein Begriff kann mehrere Erklärungslisten haben.

```html
<dl>
    <dt>Kaffee</dt>
        <dd>Schwarzes Heißgetränk aus der Kaffeebohne.</dd>
        <dd>Ein Lokal in dem Kaffee ausgeschenkt wird.</dd>
    <dt>Milch</dt>
        <dd>Weißes Kaltgetränk aus dem Euter der Kuh.</dd>
        <dd>Weiße Flüssigkeit aus Pflanzen, auch Pflanzenmilch.</dd>
</dl>
```

Voreingestellt hat der Inhalt des Elements `<dd>` einen Einzug von der linken Seite.

## Attribute

Dieses Element unterstützt [globale Attribute](../Globale_Attribute.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

## Veraltete Attribute

### nowrap

Wenn der Wert dieses Attributs auf `yes` gesetzt ist, wird der Definitionstext nicht umbrochen. Der Standardwert ist `no`.
