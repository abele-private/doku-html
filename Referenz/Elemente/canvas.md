[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<canvas>

Das `<canvas>`-Element wird zum Zeichnen von Grafiken im laufenden Betrieb über ein Skript (normalerweise JavaScript) verwendet, es ist Standardmäßig transparent.

```html
<canvas id="rectangle">
    Dieser Browser unterstützt kein JavaScript oder das canvas-Element.
</canvas>

<script>
    var canvas = document.getElementById("rectangle");
    var ctx = canvas.getContext("2d");
    ctx.fillStyle = "#FF0000";
    ctx.fillRect(0, 0, 80, 80);
</script>
```

Jeder Text innerhalb des Elements wird in Browsern mit deaktiviertem JavaScript und in Browsern, die das Element nicht unterstützen, angezeigt. Es sollte mit der Canvas-Scripting-API oder der WebGL-API verwendet werden, um Grafiken und Animationen zu zeichnen. Jedes Mal, wenn die Höhe oder Breite eines Canvas neu festgelegt wird, wird der Inhalt des Canvas gelöscht.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### height

Gibt die Höhe der Leinwand an. Standardwert ist 150 Pixel.

### width

Gibt die Breite der Leinwand an Standardwert ist 300 Pixel.
