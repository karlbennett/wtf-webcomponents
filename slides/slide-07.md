All together now
================

So EASY! Declarative programming is so GREAT!

```html
<custom name="your-tag" attibutes="heading">
  <h1>${heading}</h1>
  <p><slot></p>
</custom>

<custom name="my-tag" attibutes="colour size">
  <link rel="import" href="https://you.site/your-tag.html">
  <your-tag heading="Webcomponents">Are the best!</your-tag>
  <p style="color: ${colour}; font-size: ${size}"><slot></p>
</custom>

<html>
  <head>
    <link rel="import" href="https://my.site/my-tag.html">
  </head>
  <body>
    <my-tag colour="green" size="5em">
      I like big green text.
    </my-tag>
  </body>
</html>
```