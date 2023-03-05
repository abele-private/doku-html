[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<a>

Das `<a>`-Element ("a" für Anker, daher auch Anker-Element) stellte früher einen Ankerverweis in einem HTML-Dokument dar, auf das per vorangestelltem Hash-Zeichen (#) verwiesen werden konnte. Heute übernimmt dies das `id`-Attribut.

Alte Version:
```html
<a name="Ankername">Text</a>
<a href="#Ankername">Link</a>
```

Neue Version:
```html
<h1 id="Ankername">Text</h1>
<a href="#Ankername">Link</a>
```
Das `id`-Attribut ist global und kann in jedem Element verwendet werden.

Heute wird das `<a>`-Element immer mit dem `href`-Attribut verwendet um auf eine Webseite, Datei, E-Mail-Adresse, Telefonnummer und so weiter zu verweisen. Wenn das `href`-Attribut vorhanden ist, wird es durch Drücken der Eingabetaste (zum Beispiel Mausklick, Enter-Taste) aktiviert, während der Fokus auf dem `<a>`-Element liegt. Ein Element ohne oder mit leerem `href`-Attribut ist immer, nur ein Platzhalter für einen Link.

HTML-5-Standard:
```html
<a href="https://google.de">Google</a>
```

Standardmäßig werden Links in allen Browsern wie folgt dargestellt:

- ein nicht besuchter Link ist unterstrichen und blau
- ein besuchter Link ist unterstrichen und violett
- ein aktiver Link ist unterstrichen und rot

## Attribute

Dieses Element unterstützt [globale Attribute](../Globale_Attribute.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### href

Das `href`-Attribut gibt die URL zum Ziel an, zu der der Link führt.

Dieses Attribut ist zwingend notwendig, ohne oder mit leerem Attribut stellt das Element lediglich einen Link-Platzhalter dar und wird als normaler Text angezeigt. Soll der Platzhalter als Link angezeigt werden, kann das Hash-Zeichen (#) verwendet werden. Somit wird es als Link angezeigt, verweist aber auf kein Ziel.

```html
<a href="#">Link</a>
```

Soll auf den Seitenanfang des aktuellen Dokuments verwiesen werden, kann der Eintrag `#top` verwendet werden.

```html
<a href="#top">Link</a>
```

Verweise sind nicht auf HTTP-basierte URLs beschränkt, man kann jedes von Browsern unterstützte URL-Schema verwenden:

Eine absolute URL verweist auf eine andere Website.
```html
<a href="http://www.beispiel.de">Link</a>
```

Eine relative URL verweist auf eine Datei innerhalb einer Website.
```html
<a href="datei.html">Link</a>
```

Verweis zu einem Element mit einer bestimmten ID innerhalb der Seite.
```html
<a href="#Sektion">Link</a>
```
Bei der Verwendung von Sprungmarken wird die Datei nicht neu geladen, vielmehr springt die Anzeige im Browser zum entsprechenden Punkt im geladenen Dokument.

Verweis auf eine E-Mail-Adressen. Dabei öffnet sich der Standard-E-Mail-Client, die Adresse wird automatisch eingefügt.
```html
<a href="mailto:max@beispiel.de">E-Mail.Adresse</a>
```
Zusätzlich kann ein vordefinierter Betreff hinzugefügt werden.
```html
<a href="mailto:max@beispiel.de?subject=Betreff">E-Mail.Adresse</a>
```
Auf die selbe Weise können die Felder `cc=`, `bcc=` und `body=` mit einem `&` vorangestellt angehängt werden.
```html
<a href="mailto:max@beispiel.de?cc=muster@beispiel.de&bcc=mann@beispiel.de&subject=Betreff&body=Text">E-Mail.Adresse</a>
```

Verweis auf eine Telefonnummer.
```html
<a href="tel:+4915122233344">+49 (0)151 222 333 44</a>
```

Verweis auf eine Skript-Funktion, die beim anklicken gestartet wird.
```html
<a href="javascript:alert('Hallo');">Hallo</a>
```

Verweis zum öffnen einer Datei in einer lokalen Anwendung über den `registerProtocolHandler()`.
```html
<a href="ms-word://Datei">Word-Dokument</a>
```

### download

Das download-Attribut veranlasst den Browser, die verlinkte URL als Download zu behandeln.

Der optionale Wert des `download`-Attributs ersetzt den Name der Datei, nachdem sie heruntergeladen wurde. Es gibt keine Beschränkungen für die zulässigen Werte, der Browser erkennt automatisch die richtige Dateierweiterung und fügt sie der Datei hinzu, beziehungsweise ändert nur den Dateinamen.
```html
<a href="f00a8fg568.docx" download="Anschreiben">Datei</a>
```
Dieses Beispiel downloaded die Datei _f00a8fg568.docx_ herunter und benennt sie in _Anschreiben.docx_ um.

Wird der Wert weggelassen, wird der ursprüngliche Dateiname verwendet.
```html
<a href="f00a8fg568.docx" download>Datei</a>
```

Ohne einen Wert schlägt der Browser einen Dateinamen/eine Dateierweiterung vor, welche/n er aus verschiedenen Quellen ermittelt.

Zum Beispiel:
- aus dem HTTP-Header-Feld `Content-Disposition`
- aus dem letzte Segment im URL-Pfad
- aus dem Medientyp (aus dem HTTP-Header-Feld `Content-Type`, dem Beginn einer `data:`-URL oder dem `Blob.type` für eine `blob:`-URL
- aus dem Dateinamen (vom Dateisystem nicht unterstützte Zeichen werden vom Browser automatisch durch Unterstriche (_) ersetzt)

Wenn das `Content-Disposition`-Header-Feld andere Informationen enthält als das `download`-Attribut, kann das Verhalten unterschiedlich ausfallen:
- Wenn der Header einen Dateinamen angibt, hat er Vorrang vor einem im `download`-Attribut angegebenen Dateinamen.
- Wenn der Header eine `inline`-Disposition angibt, bevorzugen Chrome und Firefox das Attribut und behandeln es wie einen Download. Ältere Firefox-Versionen (vor 82) bevorzugen den Header und zeigen den Inhalt `inline` an.

Das `download`-Attribut kann nur auf URLs gleicher Herkunft oder den Schemata blob: und data: angewendet werden.

Wie `download` behandelt wird, hängt vom Browser, den Benutzereinstellungen und anderen Faktoren ab. Der Benutzer kann vor dem Start eines Downloads gefragt werden, die Datei wird automatisch gespeichert, oder sie wird automatisch geöffnet, entweder in einer externen Anwendung oder im Browser selbst.

### hreflang

Das `hreflang`-Attribut gibt die Sprache des verlinkten Dokuments an.

```html
<a href="text_de.docx" hreflang="de">Datei</a>
```

Erlaubte Werte sind die gleichen wie beim globalen `lang`-Attribut, ein aus zwei Buchstaben bestehender Sprachcode ([ISO 639-1](../Sprachcodes.md)). Dieses Attribut ist nur sinnvoll, wenn das `href`-Attribut auf eine Datei verweist, die Text oder Sprache enthält.

### media

Das `media`-Attribut wird verwendet, um anzugeben, dass die Ziel-URL für spezielle Geräte (wie zum Beispiel für Mobiltelefone), Sprach- oder Druckmedien konzipiert ist.

```html
<a href="seite.html" media="print">Seite</a>
```

#### Operatoren

| Wert | Beschreibung |
| ---- | ------------ |
| and | spezifiziert einen _und_ |
| not | spezifiziert einen _nicht_ |
| , | spezifiziert einen _oder_ |

#### Geräte

| Wert | Beschreibung |
| ---- | ------------ |
| all | _Standardwert_ - Bezieht sich auf alle Geräte |
| aural | Sprachgeneratoren |
| braille | Blindenschriftgeräte (Braillezeile) |
| handheld | **veraltet**, Handheld-Geräte (kleiner Bildschirm, begrenzte Bandbreite) |
| projection | Projektoren |
| print | Drucker |
| screen | Bildschirme |
| tty | **veraltet**, Fernschreiber und ähnliche Medien mit festem Zeichenraster |
| tv | Fernsehgeräte (geringe Auflösung, begrenzte Scroll-Fähigkeit) |

#### Werte

| Wert | Beschreibung |
| ---- | ------------ |
| width | Gibt die angestrebte Breite des Anzeigebereichs an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (min-width: 500px)"` |
| height | Gibt die angestrebte Höhe des Anzeigebereichs an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (max-height: 500px)"` |
| device-width | Gibt die Breite des Ziel-Displays/Papiers an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (device-width: 10cm)"` |
| device-height | Gibt die Höhe des Ziel-Displays/Papiers an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (device-height: 20cm)"` |
| orientation | Gibt die Ausrichtung des Ziel-Displays/Papiers an.<br>Mögliche Werte: `portrait` (Hochformat) oder `landscape` (Querformat)<br>Beispiel: `media="all and (orientation: landscape)"` |
| aspect-ratio | Gibt das Verhältnis zwischen Breite und Höhe des angestrebten Anzeigebereichs an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (aspect-ratio: 16/9)"` |
| device-aspect-ratio | Gibt das Verhältnis von Gerätebreite zu -höhe des Ziel-Displays/Papiers an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (device-aspect-ratio: 16/9)"` |
| color | Gibt die Bits pro Farbe der Zieldarstellung an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (color: 3)"` |
| color-index | Gibt die Anzahl der Farben an, die das Ziel-Display verarbeiten kann.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (min-color-index: 256)"` |
| monochrome | Gibt die Bits pro Pixel in einem monochromen Bildpuffer an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="screen and (monochrom: 2)"` |
| resolution | Gibt die Pixeldichte (dpi oder dpcm) des Ziel-Displays/Druckers an.<br>Es können die Präfixe `min-` und `max-` verwendet werden.<br>Beispiel: `media="print and (resolution: 300dpi)"` |
| scan | Gibt die Abtastmethode eines Fernsehbildschirms an.<br>Mögliche Werte sind `progressive` (fortlaufend) und `interlace` (verschachtelt).<br>Beispiel: `media="tv and (scan: interlace)"` |
| grid | Gibt an, ob das Ausgabegerät ein Raster oder eine Bitmap ist.<br>Mögliche Werte sind `1` für Raster und `0` andernfalls.<br>Beispiel: `media="handheld and (grid: 1)"` |

### ping

Das `ping`-Attribut gibt eine oder eine Liste von URLs an, die im Hintergrund, aufgerufen werden sollen, wenn der Link angeklickt wird.

```html
<a href="datei.jpg" ping="zähler.php">Link</a>
<a href="datei.jpg" ping="zähler1.php zähler2.php">Link</a>
```

Hierbei sendet der Browser eine HTTP-POST-Anfrage an die angegebene URL. Wird eine Liste von URLs angegeben, müssen diese durch ein Leerzeichen getrennt werden. Typischerweise wird dieses Attribut zur Nachverfolgung verwendet.

### referrerpolicy

Das `referrerpolicy`-Attribut gibt an, welche Referrer-Informationen gesendet werden sollen, wenn der Benutzer auf den Verweis klickt.

```html
<a href="https://www.beispiel.de/seite.html" referrerpolicy="no-referrer-when-downgrade">Link</a>
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
<a href="seite2.html" rel="next">Nächste Seite</a>
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

### target

Das `target`-Attribut gibt an, wo der Browser das verknüpfte Dokument öffnen soll. Ohne das Attribut wird der Verweis in der aktuellen Registerkarte geöffnet.

```html
<a href="seite.html" target="_blank">Link</a>
```

| Wert | Beschreibung |
| ---- | ------------ |
| _blank | normalerweise wird eine neue Registerkarte geöffnet, der Benutzer kann die Browser-Einstellungen so konfigurieren, dass stattdessen ein neues Fenster geöffnet wird |
| _self | öffnet das verknüpfte Dokument in demselben Rahmen, in dem es angeklickt wurde (Standardeinstellung) |
| _parent | wird in der nächsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _top | wird in der höchsten übergeordneten Anzeige-Ebene der aktuellen Anzeige geöffnet, wenn kein übergeordnete Anzeige-Ebene vorhanden ist, verhält es sich wie `_self` |
| _iFrame-Name_ | öffnet das verknüpfte Dokument in dem benannten Frame oder Iframe |

### type

Das `type`-Attribut spezifiziert den [Internet-Medien-Type](../Internet-Medien-Types.md) (früher bekannt als MIME-Type) des verlinkten Dokuments.

```html
<a href="seite.php" type="text/html">Link</a>
```

## Veraltete Attribute

### charset

Spezifiziert die Zeichenkodierung der verlinkten URL.

```html
<a href="seite.html" charset="utf-8">Link</a>
```

### coords

Das `coords`-Attribut wurde früher mit dem `shape`-Attribute in einer Image-Map verwendet. Es definiert die Koordinaten eines Link-Bereichs. Die Koordinaten werden durch ein Kommata getrennt, der Wert wird in Pixel berechnet. Die Koordinaten der linken oberen Ecke eines Bereichs sind 0,0.

```html
<img src="map.gif" type="image/gif" usemap="#map1" alt="Image Map">

<map name="map1">
    <a href="link1.html" shape="rect" coords="0,0,20,20">Link 1</a>
    <a href="link2.html" shape="rect" coords="20,0,40,20">Link 2</a>
    <a href="link3.html" shape="rect" coords="0,20,20,40">Link 3</a>
    <a href="link4.html" shape="rect" coords="00,20,40,40">Link 4</a>
</map>
```

| Wert | Beschreibung |
| ---- | ------------ |
| _x1,y1,x2,y2_ | gibt die Koordinaten der oberen linken und unteren rechten Ecke des Rechtecks an `shape="rect"` |
| _x,y,r_ | gibt die Koordinaten des Kreismittelpunkts und den Radius an `shape="circle"` |
| _x1,y1,x2,y2,xn,yn..._ | gibt die Koordinaten der Kanten des Polygons an; wenn das erste und das letzte Koordinatenpaar nicht gleich sind, fügt der Browser das letzte Koordinatenpaar hinzu, um das Polygon zu schließen `shape="poly"` |

### name

Das `name`-Attribut definiert den Namen eines Ankers (eine Sprungmarke). 

```html
<a name="Ankername">Text</a>
<a href="#Ankername">Link</a>
```

In HTML 4.01 konnten `id` und `name` zusammen auf einer Seite verwendet werden, solange sie in einem Element identische und in verschiedenen Elemente unterschiedliche Werte hatten.

### rev

Das `rev`-Attribut definiert einen Reverse-Link und gilt als die umgekehrte Beziehung des `rel`-Attributs. Das heißt, dieser Verweis zeigt auf ein Dokument, von dem auf dieses Dokument mittels `rel`-Attribut verwiesen wurde.

```html
<a href="seite.html" rev="start">Link</a>
```

| Wert | Beschreibung |
| ---- | ------------ |
| alternate | dabei kann es sich um eine druckbare Seite, das gleiche Dokument in einer anderen Sprache oder eine Kopie handeln, das eine alternative Version des aktuellen Dokuments darstellt |
| start | bezieht sich auf das erste Dokument in einer Sammlung von Dokumenten (zum Beispiel eine Index-Datei) |
| next | verweist zurück auf das nächste Dokument in einer Reihe von Dokumenten |
| prev | verweist zurück auf das vorherige Dokument in einer Reihe von Dokumenten |
| contents | Rückverweis auf das Dokument, das ein Inhaltsverzeichnis ist |
| index | verweist zurück auf das Dokument, das den Index für das aktuelle Dokument darstellt |
| glossary | verweist zurück auf das Dokument, das eine Erklärung der im aktuellen Dokument verwendeten Wörter enthält |
| copyright | verweist zurück auf die Copyright-Informationen des aktuellen Dokuments |
| chapter | verweist zurück auf das Kapitel in dem sich das aktuelle Dokument befindet  |
| section | verweist zurück auf eine Sektion/den Abschnitt in dem sich das aktuelle Dokument befindet |
| subsection | verweist zurück auf eine Untersektion/den Unterabschnitt in dem sich das aktuelle Dokument befindet |
| appendix | verweist zurück auf einen Anhang zum aktuellen Dokument |
| help | verweist zurück auf ein Hilfedokument |
| bookmark | verweist zurück auf eine permanente URL zum Setzen von Lesezeichen |

Aufgrund des exponentiellen Anstiegs der Anzahl der Verweise und Rückverweise in größeren Projekten und der daraus entstehenden Verwirrungen, wurde dieses Attribut wieder abgeschafft.

### shape

Das `shape`-Attribut wurde früher mit dem `coords`-Attribut in einer Image-Map verwendet. Es definiert die Form, der die Koordinaten folgen sollen.

```html
<img src="map.gif" type="image/gif" usemap="#map1" alt="Image Map">

<map name="map1">
    <a href="link1.html" shape="rect" coords="0,0,20,20">Link 1</a>
    <a href="link2.html" shape="rect" coords="20,0,40,20">Link 2</a>
    <a href="link3.html" shape="rect" coords="0,20,20,40">Link 3</a>
    <a href="link4.html" shape="rect" coords="00,20,40,40">Link 4</a>
</map>
```

| Wert | Beschreibung |
| ---- | ------------ |
| rect | definiert einen rechteckigen Bereich |
| circle | definiert einen kreisförmigen Bereich |
| poly | definiert einen polygonalen Bereich |
| default | definiert den gesamten Bereich |
