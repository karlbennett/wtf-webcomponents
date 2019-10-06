Shadow DOM
==========

Encapsulation is still great. But lets make it a pain to do.

```javascript
class MyTag extends HTMLElement {
  constructor() {
    super();
    this.shadow = this.attachShadow({mode: 'open'});
  }

  connectedCallback() {
    this.shadow.innerHTML = `
      <p style="color: ${this.colour}; font-size: ${this.size}">This is my tag.</p>
      <p><slot></p>
    `;
  }
}
```