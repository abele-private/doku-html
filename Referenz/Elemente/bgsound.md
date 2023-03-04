[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<bgsound>

**VERALTET**

Das `<bgsound>`-Element ist veraltet. Es richtet eine Tondatei ein, die im Hintergrund abgespielt wird, während die Seite geöffnet ist.

```html
<bgsound src="audio.mid" loop="infinite"></bgsound>
```

## Attribute

### balance

Dieses Attribut legt eine Zahl zwischen `-10,000` und `+10,000` fest, die bestimmt, wie die Lautstärke auf die Lautsprecher aufgeteilt wird.

### loop

Dieses Attribut gibt an, wie oft ein Sound abgespielt werden soll und hat entweder einen numerischen Wert oder das Schlüsselwort `infinite` (unendlich).

### src

Dieses Attribut gibt die URL der abzuspielenden Tondatei an, die einem der folgenden Typen entsprechen muss: .wav, .au oder .mid.

### volume

Dieses Attribut definiert eine Zahl zwischen `-10,000` und `0`, die die Lautstärke des Hintergrundtons einer Seite bestimmt.
