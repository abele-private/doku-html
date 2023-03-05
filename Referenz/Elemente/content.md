[Startseite](../../../../) > Referenz > [Elemente](../Elemente_Alphabetisch.md) >

# \<content>

**VERALTET**

Das `<content>`-Element ist ein veralteter Teil der _Web Components suite of technologies_ und wurde innerhalb von Shadow DOM als Einfügepunkt verwendet und war nicht für die Verwendung in normalem HTML gedacht. Es wurde durch das `<slot>`-Element ersetzt, das einen Punkt im DOM erzeugt, an dem ein Shadow DOM eingefügt werden kann.

```html
<body>
    <div>
      <h4>My Content Heading</h4>
      <p>My content text</p>
    </div>

    <script>
      const myContent = document.querySelector("div");
      const shadowroot = myContent.createShadowRoot();
      shadowroot.innerHTML = '<h2>Inserted Heading</h2> <content select="p"></content>';
    </script>
  </body>
```

## Attribute

Dieses Element unterstützt [globale Attribute](../Globale_Attribute.md).

## select

Eine kommagetrennte Liste von Selektoren. Diese haben die gleiche Syntax wie CSS-Selektoren. Sie wählen den Inhalt aus, der anstelle des `<content>`-Elements eingefügt werden soll.
