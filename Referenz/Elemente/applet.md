[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<applet>

**VERALTET**

Das `<applet>`-Element wurde verwendet, um ein eingebettetes Applet (Plug-in) zu definieren. Bereits in HTML 4.01 war dieses Element veraltet und in HTML5 ist es vollständig veraltet, stattdessen kann das `object`-Element verwendet werden.

```html
<applet code="game.class" align="center" archive="game.zip" height="250" width="350">
    <param name="difficulty" value="easy">
    <b>Sie brauchen Java, um dieses Spiel zu spielen.</b>
</applet>
```

Plug-ins wurden für viele verschiedene Zwecke verwendet:

- Ausführen von Java-Applets
- ActiveX-Steuerelemente ausführen
- Anzeige von Flash-Filmen
- Karten anzeigen
- Scannen nach Viren
- Überprüfen einer Bankverbindung

Die meisten Browser unterstützen heute keine Java-Applets, ActiveX-Steuerelemente, Plug-ins mehr und Shockwave Flash wurde eingestellt.
