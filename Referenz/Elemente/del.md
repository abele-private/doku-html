[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<del>

Das `<del>`-Element stellt einen Textbereich dar, der aus einem Dokument gelöscht wurde. Dies kann zum Beispiel bei der Darstellung von _Track Changes_ oder _Quellcode-Diff-Informationen_ verwendet werden.

```html
<p>Ein Teil <del>dieses Textes</del> ist nicht mehr richtig.</p>
```

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).

### cite

Das `cite`-Attribut gibt eine URL zu einem Dokument an, in dem der Grund für die Löschung/Änderung des Textes erläutert wird.

```html
<p>Ein Teil <del cite="grund.html">dieses Textes</del> ist nicht mehr richtig.</p>
```

### datetime

Das `datetime`-Attribut gibt die Uhrzeit und das Datum der Löschung/Änderung an und muss eine gültige Datumszeichenfolge mit einer optionalen Zeitangabe sein.

```html
<p>Ein Teil <del datetime="2023-03-22T08:05:03Z">dieses Textes</del> ist nicht mehr richtig.</p>
```

Kann der Wert nicht als Datum mit einer optionalen Zeitangabe geparst werden, hat das Element keinen zugehörigen Zeitstempel. Das Format der Zeichenfolge, wenn sie sowohl Datum als auch Uhrzeit enthält, wird als lokale Datums- und Zeitzeichenfolgen behandelt.

Datum-Uhrzeitformat: YYYY-MM-DDThh:mm:ssTZD
Datumsformat: YYYY-MM-DD

Erläuterung der Formatzeichen:

| Wert | Beschreibung |
| ---- | ------------ |
| JJJJ | vierstellige Jahreszahl (2023) |
| MM | zweistellige Monatszahl mit führender 0 (01 für Januar) |
| DD | Tageszahl im Monat (08)
| T oder Leerzeichen | Trennzeichen (erforderlich, wenn auch die Uhrzeit angegeben wird) |
| hh | Stunde mit führender 0 (08 für 8.00 Uhr)
| : | Trennzeichen |
| mm | Minuten mit führender 0 (02) |
| : | Trennzeichen |
| ss | Sekunden mit führender 0 (03) |
| TZD | Zeitzonenkennzeichen (Z steht für Zulu, auch bekannt als Greenwich Mean Time)
