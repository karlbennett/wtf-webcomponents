Shadow DOM
==========

Encapsulation? Yes please.

```html
<html>
  <head>
  </head>
  <body>
    <style>p {color: green}</style>
    <div>
      <shadow>
        <p>I'm NOT GREEN!</p>
      </shadow>
    </div>
    <div>
      <shadow>
        <style>p {color: red}</style>
        <p>I'm RED!</p>
      </shadow>
    </div>
  
    <p>I'm NOT RED! But I am green.</p>
  </body>
</html>
```
