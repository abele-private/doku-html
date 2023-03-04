[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<audio>

Das `<audio>`-Element wird verwendet, um Toninhalte in ein Dokument einzubetten, zum Beispiel Musik oder andere Audioströme. Es enthält ein oder mehrere `<source>`-Elemente mit verschiedenen Audioquellen. Der Browser wählt die erste Quelle, die er unterstützt.

```html
<audio>
    <source src="lied.mp3" type="audio/mpeg">
    Das audio-Element wird nicht unterstützt!
</audio>
```

Es gibt drei unterstützte Audioformate in HTML: MP3, WAV und OGG. Der Inhalt innerhalb der öffnenden und schließenden `<audio> … </audio>`-Tags wird in Browsern, die das Element nicht unterstützen, als Fallback (Rückfall) angezeigt.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### autoplay

Das `autoplay`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn dieses Attribut gesetzt wird, beginnt die Audiowiedergabe automatisch, sobald der Browser dazu in der Lage ist, ohne zu warten, bis das Herunterladen der gesamten Audiodatei abgeschlossen ist.

```html
<audio autoplay>
    <source src="lied.mp3" type="audio/mpeg">
    Das audio-Element wird nicht unterstützt!
</audio>
```

Einige Browser lassen standardmäßig `autoplay` in den meisten Fällen nicht zu, beziehungsweise können so eingestellt werden. Wenn man das Attribut `muted` nach `autoplay` hinzufügt, spielen einige Browser das Audio trotzdem automatisch ab.

Websites, die automatisch Audiodateien (oder Videos mit einer Tonspur) abspielen, können für die Nutzer eine unangenehme Erfahrung sein und sollten daher nach Möglichkeit vermieden werden. Wenn man die Autoplay-Funktion anbieten möchte, sollte man diese nur auf Wunsch des Benutzers aktivieren (das heißt er muss sie selbst starten).

### controls

Das `controls`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn dieses Attribut gesetzt wird, gibt es an, dass der Browser Audio-Steuerelemente anzeigen soll.

```html
<audio controls>
    <source src="lied.mp3" type="audio/mpeg">
    Das audio-Element wird nicht unterstützt!
</audio>
```

Audio-Steuerelemente umfassen unter anderem folgende Schaltflächen:
- Play
- Pause
- Suchlauf
- Lautstärke

### loop

Das `loop`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn dieses Attribut gesetzt wird, gibt es an, dass das Audio immer wieder von vorne beginnt, wenn es zu Ende ist.

```html
<audio loop>
    <source src="lied.mp3" type="audio/mpeg">
    Das audio-Element wird nicht unterstützt!
</audio>
```

### muted

Das `muted`-Attribut ist ein boolesches Attribut, es benötigt keinen Wert. Wenn dieses Attribut gesetzt wird, gibt es an, dass die Audioausgabe stummgeschaltet werden soll.

```html
<audio muted>
    <source src="lied.mp3" type="audio/mpeg">
    Das audio-Element wird nicht unterstützt!
</audio>
```

### preload

Das `preload`-Attribut gibt an, ob und wie die Audiodatei beim Laden der Seite geladen werden soll.

```html
<audio preload="auto">
    <source src="lied.mp3" type="audio/mpeg">
    Das audio-Element wird nicht unterstützt!
</audio>
```

| Wert | Beschreibung |
| ---- | ------------ |
| none | gibt an, dass das die Datei nicht vorgeladen werden soll |
| metadata | gibt an, dass nur Audio-Metadaten (zum Beispiel die Länge) abgerufen werden, nicht aber die ganze Datei |
| auto | gibt an, dass die gesamte Audiodatei heruntergeladen werden kann, auch wenn der Benutzer sie nicht verwendet |
| _ohne Wert_ | ein Synonym für den Wert `auto` |

Der Standardwert ist für jeden Browser unterschiedlich. Die Spezifikation rät, ihn auf `metadata` zu setzen.

Das Attribut `autoplay` hat Vorrang vor `preload`. Wenn `autoplay` angegeben ist, müsste der Browser mit dem Herunterladen der Datei für die Wiedergabe beginnen. Der Browser ist durch die Spezifikation nicht gezwungen, dem Wert dieses Attributs zu folgen.

### src

Das `src`-Attribut gibt den Speicherort (URL) der Audiodatei an. Dieses Attribut ist optional und nur sinnvoll wenn eine einzige Datei zur Verfügung steht.

```html
<audio src="lied.mp3">
    Das audio-Element wird nicht unterstützt!
</audio>
```

Stehen mehrere Dateiversionen zur Verfügung, kann stattdessen das `<source>`-Element innerhalb des `<audio>`-Blocks verwendet werden, um das einzubettende Audiomaterial anzugeben. Jedes `<source>`-Element kann auf eine andere Audiodatei verweisen. Der Browser wird das erste unterstützte Format verwenden.
