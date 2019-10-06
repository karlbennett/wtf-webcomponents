Custom Elements
===============

What a novel idea!

```html
<html>
  <head>
  </head>
  <body>
    <custom name="my-tag" attibutes="colour size">
      <p style="color: ${colour}; font-size: ${size}">
        This is my tag.
      </p>
      <p><slot></p>
    </custom>
  
    <my-tag colour="red" size="20px">Some text.</my-tag>
  </body>
</html>
```