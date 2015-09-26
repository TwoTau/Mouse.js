# MouseJS
A very small JavaScript library that allows you to track a client's cursor position on an element

You can initialize it with some HTML and JavaScript:
```html
<script src="https://raw.githubusercontent.com/TwoTau/MouseJS/master/Mouse.js"></script>
```
```javascript
var mouse = new MouseJS(someElement);
```
You can find
* Where the user's mouse position with `mouse.x``` and ```mouse.y`
* Where the user last left clicked with `mouse.left.before.x`
* When the user last pressed down their left mouse button with `mouse.left.clickTime`
* When the user last released their left mouse button with `mouse.left.releaseTime`
* And the same for the right mouse button

All MouseJS times are formatted in milliseconds since the object's initialization. For example:
```js
console.log(mouse.right.clickTime); // might be something like 1250 (for 1.25 seconds)
```

You can tell if the client's left mouse button is down with:
```js
console.log(mouse.left.releaseTime < mouse.getTime())
```

Note that the HTML element has to have `focus` for MouseJS to be able to track the client's mouse. You can force an element to have focus with
```js
someElement.focus();
```
