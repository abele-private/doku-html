[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<base>

Das `<base>`-Element gibt die Basis-URL und/oder das Ziel für alle relativen URLs in einem Dokument an. Es muss immer ein `href`- oder ein `target`-Attribut gesetzt sein, oder beide.

```html
<head>
    <base href="https://www.domain.de/" target="_blank">
</head>
```

Es darf nur ein einziges `<base>`-Element in einem Dokument geben, und es muss sich innerhalb des `<head>`-Elements befinden. Dieses Element muss vor allen anderen Elementen mit URL-Attributwerten stehen.

## Attribute

Dieses Element unterstützt [globale Attribute](../Globale_Attribute.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### href

Das `href`-Attribut gibt die Basis-URL für alle relativen Verweise an.

```html
<head>
    <base href="https://www.domain.de/">
</head>
```

### target

Das `target`-Attribut gibt an, wo der Browser die Verweise öffnen soll. Ohne das Attribut werden die Verweise in der aktuellen Registerkarte geöffnet.

```html
<head>
    <base target="_blank">
</head>
```

| Wert | Beschreibung |
| ---- | ------------ |
| _blank | normalerweise wird eine neue Registerkarte geöffnet, der Benutzer kann die Browser-Einstellungen so konfigurieren, dass stattdessen ein neues Fenster geöffnet wird |
| _self | öffnet das verknüpfte Dokument in demselben Rahmen, in dem es angeklickt wurde (Standardeinstellung) |
| _parent | wird in der nächsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _top | wird in der höchsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
