[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<datalist>

Das `<datalist>`-Element gibt eine Liste von vordefinierten Optionen für ein Eingabeelement an. Es wird verwendet, um eine "Autovervollständigungsfunktion" für Eingabeelemente bereitzustellen. Bei der Dateneingabe wird den Benutzern eine Dropdown-Liste mit vordefinierten Optionen angezeigt.

```html
<label for="browser">Wähle einen Browser aus:</label>
<input list="browsers" name="browser" id="browser">

<datalist id="browsers">
    <option value="Edge">
    <option value="Firefox">
    <option value="Chrome">
    <option value="Opera">
    <option value="Safari">
</datalist>
```

Das `id`-Attribut des `<datalist>`-Elements muss gleich dem `list`-Attribut des `<input>`-Elements sein (dadurch werden sie miteinander verbunden).

Vorbestimmte Varianten für die Eingabe werden im eingeschlossenen `<option>`-Element platziert. Die Varianten werden nur dann sichtbar, wenn der Benutzer die Texteingabe startet.

## Attribute

Dieses Element unterstützt [globale Attribute](../Elemente_Alphabetisch.md).

Dieses Element unterstützt [Ereignisattribute](../Ereignisattribute.md).
