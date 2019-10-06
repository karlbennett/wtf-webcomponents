Custom Elements
===============

Why build HTML with HTML, when you can use JAVASCRIPT!

Not this.
```html
<custom name="my-tag" attibutes="colour size">
  <p style="color: ${colour}; font-size: ${size}">This is my tag.</p>
  <p><slot></p>
</custom>
```


But THIS!
```javascript
class MyTag extends HTMLElement {
  constructor() {
    super();
    this.shadow = this.attachShadow({mode: 'open'});
  }

  connectedCallback() {
    this.shadow.innerHTML = `
      <p style="color: ${this.colour}; font-size: ${this.size}">
        This is my tag.
      </p>
      <p><slot></p>
    `;
  }

  get colour() {
    return this.getAttribute('colour');
  }

  set colour(colour) {
    this.setAttribute('colour', colour);
  }

  get size() {
    return this.getAttribute('size');
  }

  set size(size) {
    this.setAttribute('size', size);
  }
}
customElements.define('my-tag', MyTag);
```