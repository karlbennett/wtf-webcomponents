Shadow DOM
==========

Encapsulation? Yes please.

```html
<html>
  <head>
  </head>
  <body>
    <div>
      <shadow>
        <style>p {color: red}</style>
        <p>I'm RED!</p>
      </shadow>
    </div>
  
    <p>I'm NOT RED!</p>
  </body>
</html>
```