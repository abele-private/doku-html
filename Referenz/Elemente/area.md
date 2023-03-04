[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<area>

Das `<area>`-Element definiert einen Bereich innerhalb einer Image-Map. Es befindet sich ausschließlich innerhalb eines `<map>`-Elements.

```html
<img src="map.gif" type="image/gif" usemap="#map1" alt="Image Map">

<map name="map1">
    <area href="link1.html" shape="rect" coords="0,0,20,20" alt="Seite 1">
    <area href="link2.html" shape="rect" coords="20,0,40,20" alt="Seite 2">
    <area href="link3.html" shape="rect" coords="0,20,20,40" alt="Seite 3">
    <area href="link4.html" shape="rect" coords="00,20,40,40" alt="Seite 4">
</map>
```

Das `<area>`-Element bestimmt die aktiven Bereiche einer Image-Map (Koordinate, Form, Größe und so weiter), die durch das `<map>`-Element definiert wird. Durch den Klick auf den aktiven Bereich der Grafik wird das Ziel geöffnet. Dabei können sich die aktiven Bereiche einander überdecken. In diesem Fall wird der Bereich aktiviert, der Im HTML-Code höher liegt.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### alt

Das `alt`-Attribut gibt einen alternativen Text für einen Bereich an, wenn das Bild nicht angezeigt werden kann.

```html
<area href="deutschland.html" alt="Informationen zu Deutschland">
```

Der Text sollte so formuliert sein, dass er dem Nutzer die gleiche Art von Auswahlmöglichkeit bietet, die das Bild bietet, wenn es ohne den alternativen Text angezeigt würde.

### coords

Das `coords`-Attribut spezifiziert die Koordinaten eines Bereichs in einer Image-Map. Es wird immer zusammen mit dem `shape`-Attribut verwendet, um die Größe, Form und Platzierung eines Bereichs festzulegen. Die Koordinaten werden durch ein Kommata getrennt, der Wert wird in Pixel berechnet.

```html
<img src="map.gif" type="image/gif" usemap="#map1" alt="Image Map">

<map name="map1">
    <area href="link1.html" shape="rect" coords="0,0,20,20" alt="Seite 1">
    <area href="link2.html" shape="rect" coords="20,0,40,20" alt="Seite 2">
    <area href="link3.html" shape="rect" coords="0,20,20,40" alt="Seite 3">
    <area href="link4.html" shape="rect" coords="00,20,40,40" alt="Seite 4">
</map>
```

Die Koordinaten der linken oberen Ecke eines Bereichs sind 0,0. Dieses Attribut darf nicht verwendet werden, wenn `shape` auf `default` gesetzt wurde.

| Wert | Beschreibung |
| ---- | ------------ |
| _x1,y1,x2,y2_ | gibt die Koordinaten der oberen linken und unteren rechten Ecke des Rechtecks an `shape="rect"` |
| _x,y,r_ | gibt die Koordinaten des Kreismittelpunkts und den Radius an `shape="circle"` |
| _x1,y1,x2,y2,xn,yn..._ | gibt die Koordinaten der Kanten des Polygons an; wenn das erste und das letzte Koordinatenpaar nicht gleich sind, fügt der Browser das letzte Koordinatenpaar hinzu, um das Polygon zu schließen `shape="poly"` |

### download

Das download-Attribut veranlasst den Browser, die verlinkte URL als Download zu behandeln.

Der optionale Wert des `download`-Attributs ersetzt den Name der Datei, nachdem sie heruntergeladen wurde. Es gibt keine Beschränkungen für die zulässigen Werte, der Browser erkennt automatisch die richtige Dateierweiterung und fügt sie der Datei hinzu, beziehungsweise ändert nur den Dateinamen.
```html
<area href="f00a8fg568.docx" download="Anschreiben">
```
Dieses Beispiel downloaded die Datei _f00a8fg568.docx_ herunter und benennt sie in _Anschreiben.docx_ um.

Wird der Wert weggelassen, wird der ursprüngliche Dateiname verwendet.
```html
<area href="f00a8fg568.docx" download>
```

Eine genauere Beschreibung des `download`-Attributs befindet sich auf der Seite des [\<a>](./a.md#download)-Elements.

### href

Das `href`-Attribut gibt die URL zum Ziel an, zu der der Link führt.

Dieses Attribut ist zwingend notwendig, ohne oder mit leerem Attribut stellt das Element lediglich einen Link-Platzhalter dar und wird als normaler Text angezeigt. Soll der Platzhalter als Link angezeigt werden, kann das Hash-Zeichen (#) verwendet werden. Somit wird es als Link angezeigt, verweist aber auf kein Ziel.

```html
<area href="seite.html">
```

Eine genauere Beschreibung des `href`-Attributs befindet sich auf der Seite des [\<a>](./a.md#href)-Elements.

### hreflang

Das `hreflang`-Attribut gibt die Sprache des verlinkten Dokuments an.

```html
<area href="text_de.docx" hreflang="de">
```

Erlaubte Werte sind die gleichen wie beim globalen `lang`-Attribut, ein aus zwei Buchstaben bestehender Sprachcode ([ISO 639-1](../Sprachcodes.md)). Dieses Attribut ist nur sinnvoll, wenn das `href`-Attribut auf eine Datei verweist, die Text oder Sprache enthält.

### media

Das `media`-Attribut wird verwendet, um anzugeben, dass die Ziel-URL für spezielle Geräte (wie zum Beispiel für Mobiltelefone), Sprach- oder Druckmedien konzipiert ist.

```html
<area href="seite.html" media="print">
```

Eine genauere Beschreibung des `media`-Attributs befindet sich auf der Seite des [\<a>](./a.md#media)-Elements.

### referrerpolicy

Das `referrerpolicy`-Attribut gibt an, welche Referrer-Informationen gesendet werden sollen, wenn der Benutzer auf den Verweis klickt.

```html
<area href="https://www.beispiel.de/seite.html" referrerpolicy="no-referrer-when-downgrade">
```

| Wert | Beschreibung |
| ---- | ------------ |
| no-referrer | Es werden keine Referrer-Informationen gesendet, beziehungsweise es wird das `Referer`-Feld dem HTTP-Header nicht hinzugefügt. |
| no-referrer-when-downgrade | _Standardwert_ - Sendet den Ursprung, den Pfad und den Query-String, wenn die Protokollsicherheitsstufe gleich bleibt oder höher ist (HTTP zu HTTP, HTTPS zu HTTPS, HTTP zu HTTPS). Bei geringerer Sicherheitsstufe wird nichts gesendet (HTTPS zu HTTP). |
| origin | Der gesendete `Referer`-Feld wird auf den Ursprung der verweisenden Seite beschränkt: ihr Schema, ihr Host und ihr Port. |
| origin-when-cross-origin | Der Referrer, der an andere Ziele gesendet wird, wird auf das Schema, den Host und den Port beschränkt. Navigationen auf demselben Ursprung (`same-origin`) enthalten weiterhin den Pfad. |
| same-origin | Sendet einen Referrer für Anfragen an denselben Ursprung. Sendet keinen Referrer für herkunftsübergreifende Anfragen. |
| strict-origin | Der Ursprung des Dokuments wird nur dann als Referrer gesendet, wenn die Sicherheitsstufe des Protokolls gleich bleibt (HTTPS zu HTTPS), aber nicht an ein weniger sicheres Ziel (HTTPS zu HTTP) gesendet wird. |
| strict-origin-when-cross-origin | _Standardwert_ - Sendet eine vollständige URL, wenn die Protokollsicherheitsstufe gleich bleibt oder höher ist (HTTP zu HTTP, HTTPS zu HTTPS, und HTTP zu HTTPS). Bei geringerer Sicherheitsstufe (HTTPS zu HTTP) wird nichts gesendet. |
| unsafe-url | Der Verweis enthält den Ursprung und den Pfad (aber nicht das Fragment, das Passwort oder den Benutzernamen). **Dieser Wert ist unsicher**, da er Herkunft und Pfad von TLS-geschützten Ressourcen an unsichere Quellen weiterleitet. |

### rel

Das `rel`-Attribut spezifiziert die Beziehung zwischen dem aktuellen Dokument und dem verlinkten Dokument. Es können mehrere, durch Leerzeichen getrennte, Link-Typen verwendet werden.

```html
<area href="seite2.html" rel="next">
```

Suchmaschinen können dieses Attribut verwenden, um mehr Informationen über einen Link zu erhalten.

| Wert | Beschreibung |
| ---- | ------------ |
| alternate | enthält einen Verweis zu einer alternativen Darstellung des Dokuments (zum Beispiel Druckseite, Übersetzung oder Kopie) |
| author | enthält einen Verweis zum Autor des Dokuments |
| bookmark | permanente URL zum Setzen von Lesezeichen |
| external | zeigt an, dass das referenzierte Dokument nicht zu derselben Website gehört wie das aktuelle Dokument |
| help | enthält einen Verweis zu einem Hilfedokument |
| license | bietet einen Verweis auf die Lizenzierungsinformationen für das Dokument |
| next | bietet einen Link zum nächsten Dokument der Reihe |
| nofollow | Verweis zu einem nicht bestätigten Dokument, wie ein bezahlter Link (`nofollow` wird von Google verwendet, um anzugeben, dass der Google-Crawler diesem Link nicht folgen soll) |
| noopener | erfordert, dass ein durch das Verfolgen des Verweises erzeugter Browsing-Kontext keinen offenen Browsing-Kontext haben darf |
| noreferrer | macht den Referrer unbekannt. Es wird kein `Referer`-Feld in den HTTP-Header eingefügt, wenn der Benutzer auf den Verweis klickt |
| prev | das vorherige Dokument in einer Auswahl |
| search | Verweis zu einer Suchfunktion für das Dokument |
| tag | ein Etikett (Schlüsselwort) für das aktuelle Dokument |

### shape

Das `shape`-Attribut spezifiziert die Form eines Bereichs. Es wird zusammen mit dem `coords`-Attribut verwendet, um die Größe, Form und Platzierung eines Bereichs anzugeben.

```html
<img src="map.gif" type="image/gif" usemap="#map1" alt="Image Map">

<map name="map1">
    <area href="link1.html" shape="rect" coords="0,0,20,20" alt="Seite 1">
    <area href="link2.html" shape="rect" coords="20,0,40,20" alt="Seite 2">
    <area href="link3.html" shape="rect" coords="0,20,20,40" alt="Seite 3">
    <area href="link4.html" shape="rect" coords="00,20,40,40" alt="Seite 4">
</map>
```

Das `coords`-Attribut darf nicht verwendet werden, wenn `shape` auf `default` gesetzt wurde.

| Wert | Beschreibung |
| ---- | ------------ |
| rect | definiert einen rechteckigen Bereich |
| circle | definiert einen kreisförmigen Bereich |
| poly | definiert einen polygonalen Bereich |
| default | definiert den gesamten Bereich |

### target

Das `target`-Attribut gibt an, wo der Browser das verknüpfte Dokument öffnen soll. Ohne das Attribut wird der Verweis in der aktuellen Registerkarte geöffnet.

```html
<area href="seite.html" target="_blank">
```

| Wert | Beschreibung |
| ---- | ------------ |
| _blank | normalerweise wird eine neue Registerkarte geöffnet, der Benutzer kann die Browser-Einstellungen so konfigurieren, dass stattdessen ein neues Fenster geöffnet wird |
| _self | öffnet das verknüpfte Dokument in demselben Rahmen, in dem es angeklickt wurde (Standardeinstellung) |
| _parent | wird in der nächsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _top | wird in der höchsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _Frame-Name_ | öffnet das verknüpfte Dokument in dem benannten Frame oder Iframe |

### type

Das `type`-Attribut spezifiziert den [Internet-Medien-Type](../Internet-Medien-Types.md) (früher bekannt als MIME-Type) des verlinkten Dokuments.

```html
<area href="seite.php" type="text/html">
```

## Veraltete Attribute

### name

Definiert einen Namen für den anklickbaren Bereich, damit ältere Browser das Element mit einem Skript ansprechen können.

```html
<area href="seite.html" name="bereich1">
```

### nohref

Das `nohref`-Attribut sollte anzeigen, dass für den zugehörigen Bereich kein Hyperlink existiert. Das `nohref`-Attribut ist nicht erforderlich, da das Weglassen des `href`-Attributs ausreicht.
