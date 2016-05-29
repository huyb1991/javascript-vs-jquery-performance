# Performance Comparison of JavaScript and jQuery
Performance comparsion of **`native JavaScript`** and **`jQuery (version 2.1.0)`** follow [You might not need jquery](http://youmightnotneedjquery.com/).

The numbers at the right of links are the result of execute time with the same function for **1,000** loops of `Native JavaScript / jQuery`.
## Index
### Ajax
* <a href="#json-comparsion">JSON</a>
* <a href="#post-comparsion">Post</a>
* <a href="#request-comparsion">Request</a>

### Effects
* <a href="#fade-in-comparsion">Fade In</a> (11 ms / 269 ms)
* <a href="#hide-comparsion">Hide</a> (1.195 ms / 28.484 ms)
* <a href="#show-comparsion">Show</a> (0.765 ms / 5.179 ms)

### Elements
* <a href="#add-class-comparsion">Add Class</a> (0.740 ms / 5.649 ms)
* <a href="#after-comparsion">After</a> (3.569 ms / 45.005 ms)
* <a href="#append-comparsion">Append</a> (0.650 ms / 62.530 ms)
* <a href="#before-comparsion">Before</a> (3.225 ms / 27.440 ms)
* <a href="#children-comparsion">Children</a> (0.279 ms / 7.029 ms)
* <a href="#clone-comparsion">Clone</a> (4.934 ms / 42.889 ms)
* <a href="#contains-comparsion">Contains</a> (0.934 ms / 1.605 ms)
* <a href="#contains-selector-comparsion">Contains Selector</a> (0.604 ms / 5.759 ms)
* <a href="#each-comparsion">Each</a> (4.120 ms / 8.220 ms)
* <a href="#empty-comparsion">Empty</a> (1.969 ms / 3.639 ms)
* <a href="#filter-comparsion">Filter</a> (2.709 ms / 9.860 ms)
* <a href="#find-children-comparsion">Find Children</a>
* <a href="#find-elements-comparsion">Find Elements</a>
* <a href="#get-attributes-comparsion">Get Attributes</a>
* <a href="#get-html-comparsion">Get Html</a>
* <a href="#get-outer-html-comparsion">Get Outer Html</a>
* <a href="#get-style-comparsion">Get Style</a>
* <a href="#get-text-comparsion">Get Text</a>
* <a href="#has-class-comparsion">Has Class</a>
* <a href="#matches-comparsion">Matches</a>
* <a href="#matches-selector-comparsion">Matches Selector</a>
* <a href="#next-comparsion">Next</a>
* <a href="#offset-comparsion">Offset</a>
* <a href="#offset-parent-comparsion">Offset Parent</a>
* <a href="#outer-height-comparsion">Outer Height</a>
* <a href="#outer-height-with-margin-comparsion">Outer Height With Margin</a>
* <a href="#outer-width-comparsion">Outer Width</a>
* <a href="#outer-width-with-margin-comparsion">Outer Width With Margin</a>
* <a href="#parent-comparsion">Parent</a>
* <a href="#position-comparsion">Position</a>
* <a href="#position-relative-to-viewport-comparsion">Position Relative To Viewport</a>
* <a href="#prepend-comparsion">Prepend</a>
* <a href="#prev-comparsion">Prev</a>
* <a href="#remove-comparsion">Remove</a>
* <a href="#remove-class-comparsion">Remove Class</a>
* <a href="#replace-from-html-comparsion">Replace From Html</a>
* <a href="#set-attributes-comparsion">Set Attributes</a>
* <a href="#set-html-comparsion">Set Html</a>
* <a href="#set-style-comparsion">Set Style</a>
* <a href="#set-text-comparsion">Set Text</a>
* <a href="#siblings-comparsion">Siblings</a>
* <a href="#toggle-class-comparsion">Toggle Class</a>

### Events
* <a href="#off-comparsion">Off</a>
* <a href="#on-comparsion">On</a>
* <a href="#ready-comparsion">Ready</a>
* <a href="#trigger-custom-comparsion">Trigger Custom</a>
* <a href="#trigger-native-comparsion">Trigger Native</a>

### Utils
* <a href="#bind-comparsion">Bind</a>
* <a href="#array-each-comparsion">Array Each</a>
* <a href="#deep-extend-comparsion">Deep Extend</a>
* <a href="#extend-comparsion">Extend</a>
* <a href="#index-of-comparsion">Index Of</a>
* <a href="#is-array-comparsion">Is Array</a>
* <a href="#map-comparsion">Map</a>
* <a href="#now-comparsion">Now</a>
* <a href="#parse-html-comparsion">Parse Html</a>
* <a href="#parse-json-comparsion">Parse Json</a>
* <a href="#trim-comparsion">Trim</a>
* <a href="#type-comparsion">Type</a>

## AJAX Comparsion
### JSON Comparsion
(Updating)
### Post Comparsion
(Updating)
### Request Comparsion
(Updating)
## EFFECTS Comparsion
### Fade In Comparsion
Live code at [https://jsfiddle.net/dda467b1/1/](https://jsfiddle.net/dda467b1/1/)

`Native JavScript` take about **11** milliseconds / `jQuery` take about **269** milliseconds.
##### `Native JavScript code`
```js
function fadeIn(el) {
  el.style.opacity = 0;

  var last = +new Date(),
  var tick = function() {
    el.style.opacity = +el.style.opacity + (new Date() - last) / 400;
    last = +new Date();

    if (+el.style.opacity < 1) {
      (window.requestAnimationFrame && requestAnimationFrame(tick)) || setTimeout(tick, 16);
    }
  };

  tick();
}

fadeIn(el);
```
##### `jQuery code`
```
$(el).fadeIn();
```
### Hide Comparsion
Live code at [https://jsfiddle.net/dda467b1/2/](https://jsfiddle.net/dda467b1/2/)

`Native JavScript` take about **1.195** milliseconds / `jQuery` take about **28.484** milliseconds.
##### `Native JavScript code`
```js
el.style.display = 'none';
```
##### `jQuery code`
```
$(el).hide();
```
### Show Comparsion
Live code at [https://jsfiddle.net/dda467b1/3/](https://jsfiddle.net/dda467b1/3/)

`Native JavScript` take about **0.765** milliseconds / `jQuery` take about **25.179** milliseconds.
##### `Native JavScript code`
```js
el.style.display = ''
```
##### `jQuery code`
```
$(el).show();
```
## ELEMENTS Comparsion
### Add Class Comparsion
Live code at [https://jsfiddle.net/dda467b1/4/](https://jsfiddle.net/dda467b1/4/)

`Native JavScript` take about **0.764** milliseconds / `jQuery` take about **5.649** milliseconds.
##### `Native JavScript code`
```js
if (el.classList)
  el.classList.add(className);
else
  el.className += ' ' + className;
```
##### `jQuery code`
```
$(el).addClass(className);
```
### After Comparsion
Live code at [https://jsfiddle.net/dda467b1/5/](https://jsfiddle.net/dda467b1/5/)

`Native JavScript` take about **3.569** milliseconds / `jQuery` take about **45.005** milliseconds.
##### `Native JavScript code`
```js
el.insertAdjacentHTML('afterend', htmlString);
```
##### `jQuery code`
```
$(el).after(htmlString);
```
### Append Comparsion
Live code at [https://jsfiddle.net/dda467b1/6/](https://jsfiddle.net/dda467b1/6/)

`Native JavScript` take about **0.650** milliseconds / `jQuery` take about **62.530** milliseconds.
##### `Native JavScript code`
```js
parent.appendChild(el);
```
##### `jQuery code`
```
$(parent).append(el);
```
### Before Comparsion
Live code at [https://jsfiddle.net/dda467b1/7/](https://jsfiddle.net/dda467b1/7/)

`Native JavScript` take about **3.225** milliseconds / `jQuery` take about **27.440** milliseconds.
##### `Native JavScript code`
```js
el.insertAdjacentHTML('beforebegin', htmlString);
```
##### `jQuery code`
```
$(el).before(htmlString);
```
### Children Comparsion
Live code at [https://jsfiddle.net/dda467b1/8/](https://jsfiddle.net/dda467b1/8/)

`Native JavScript` take about **0.279** milliseconds / `jQuery` take about **7.029** milliseconds.
##### `Native JavScript code`
```js
el.children
```
##### `jQuery code`
```
$(el).children();
```
### Clone Comparsion
Live code at [https://jsfiddle.net/dda467b1/9/](https://jsfiddle.net/dda467b1/9/)

`Native JavScript` take about **4.934** milliseconds / `jQuery` take about **42.889** milliseconds.
##### `Native JavScript code`
```js
el.cloneNode(true);
```
##### `jQuery code`
```
$(el).clone();
```
### Contains Comparsion
Live code at [https://jsfiddle.net/dda467b1/11/](https://jsfiddle.net/dda467b1/11/)

`Native JavScript` take about **0.934** milliseconds / `jQuery` take about **1.605** milliseconds.
##### `Native JavScript code`
```js
el !== child && el.contains(child);
```
##### `jQuery code`
```
$.contains(el, child);
```
### Contains Selector Comparsion
Live code at [https://jsfiddle.net/dda467b1/12/](https://jsfiddle.net/dda467b1/12/)

`Native JavScript` take about **0.604** milliseconds / `jQuery` take about **5.759** milliseconds.
##### `Native JavScript code`
```js
el.querySelector(selector).length;
```
##### `jQuery code`
```
$(el).find(selector).length;
```
### Each Comparsion
Live code at [https://jsfiddle.net/dda467b1/13/](https://jsfiddle.net/dda467b1/13/)

`Native JavScript` take about **4.120** milliseconds / `jQuery` take about **8.220** milliseconds.
##### `Native JavScript code`
```js
var elements = document.querySelectorAll(selector);
Array.prototype.forEach.call(elements, function(el, i){
  // Do something
});
```
##### `jQuery code`
```
$(selector).each(function(i, el){
  // Do something
});
```
### Empty Comparsion
Live code at [https://jsfiddle.net/dda467b1/14/](https://jsfiddle.net/dda467b1/14/)

`Native JavScript` take about **1.969** milliseconds / `jQuery` take about **3.639** milliseconds.
##### `Native JavScript code`
```js
el.innerHTML = '';
```
##### `jQuery code`
```
$(el).empty();
```
### Filter Comparsion
Live code at [https://jsfiddle.net/dda467b1/15/](https://jsfiddle.net/dda467b1/15/)

`Native JavScript` take about **2.709** milliseconds / `jQuery` take about **9.860** milliseconds.
##### `Native JavScript code`
```js
Array.prototype.filter.call(document.querySelectorAll(selector), filterFn);
```
##### `jQuery code`
```
$(selector).filter(filterFn);
```
### Find Children Comparsion
(Updating)
### Find Elements Comparsion
(Updating)
### Get Attributes Comparsion
(Updating)
### Get Html Comparsion
(Updating)
### Get Outer Html Comparsion
(Updating)
### Get Style Comparsion
(Updating)
### Get Text Comparsion
(Updating)
### Has Class Comparsion
(Updating)
### Matches Comparsion
(Updating)
### Matches Selector Comparsion
(Updating)
### Next Comparsion
(Updating)
### Offset Comparsion
(Updating)
### Offset Parent Comparsion
(Updating)
### Outer Height Comparsion
(Updating)
### Outer Height With Margin Comparsion
(Updating)
### Outer Width Comparsion
(Updating)
### Outer Width With Margin Comparsion
(Updating)
### Parent Comparsion
(Updating)
### Position Comparsion
(Updating)
### Position Relative To Viewport Comparsion
(Updating)
### Prepend Comparsion
(Updating)
### Prev Comparsion
(Updating)
### Remove Comparsion
(Updating)
### Remove Class Comparsion
(Updating)
### Replace From Html Comparsion
(Updating)
### Set Attributes Comparsion
(Updating)
### Set Html Comparsion
(Updating)
### Set Style Comparsion
(Updating)
### Set Text Comparsion
(Updating)
### Siblings Comparsion
(Updating)
### Toggle Class Comparsion
(Updating)
## EVENTS Comparsion
### Off Comparsion
(Updating)
### On Comparsion
(Updating)
### Ready Comparsion
(Updating)
### Trigger Custom Comparsion
(Updating)
### Trigger Native Comparsion
(Updating)
## UTILS Comparsion
### Bind Comparsion
(Updating)
### Array Each Comparsion
(Updating)
### Deep Extend Comparsion
(Updating)
### Extend Comparsion
(Updating)
### Index Of Comparsion
(Updating)
### Is Array Comparsion
(Updating)
### Map Comparsion
(Updating)
### Now Comparsion
(Updating)
### Parse Html Comparsion
(Updating)
### Parse Json Comparsion
(Updating)
### Trim Comparsion
(Updating)
### Type Comparsion
(Updating)