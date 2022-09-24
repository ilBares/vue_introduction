# Vue js
Data and DOM are linked and everything is reactive.  
__Rectivity__ meas that Vue automatically tracks JavaScript state changes and efficiently updates the DOM when changes happan.
## Directives
Directives are special attributes provided by Vue and they apply special reactive behavior to the rendered DOM.  
Directive structure:
<pre>v-[directive name]:[argument name]</pre>  
#### Main directives:  
- __v-bind__ (:)<pre>keeps the referred element up-to-date</pre>
- __v-if__<pre>toggles the precence of an element</pre>
- __v-show__<pre>show an element only if the condition is true</pre>
- __v-for__<pre>used for displaying a list of items using the data from an Array</pre>
- __v-on__<pre>attaches event listeners that invoke methods on our Vue instances. It listens for specific events (like "clicl")</pre>
- __v-model__<pre>it makes two-way binging between element and data</pre>

### Components
> The components system is an abstraction that allows us to build large-scale applications composed of small and reusable components.
> Vue component model allow us to encapsulate custom content and logic in each component.

# Vue 2
To add Vue framework to the project:  
```html
<!-- .html -->
<!-- development version, includes helpful console warnings -->
<script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>

<!-- production version, optimized for size and speed -->
<script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
```
___

To create a Vue 2 app:  
```javascript
// .js
var app = new Vue({
  el: '#app', // attaches itself to a single DOM element, then fully controls it
  data: {
    message: 'Hello Vue!'
  }
})
```

In the index.html you have to write:  
```html
<!-- .html -->
<script src="main.js"></script>
```
___
To define a new component called todo-item:  
```javascript
// Define a new component called todo-item
Vue.component('todo-item', {
  template: '<li>This is a todo</li>'
})

var app = new Vue(...)
```
___
___

# Vue 3
> Vue 3 supports __Single-File Component__, or __SFC__ files (*.vue). It encapsulates the component's logic (Javascript), template (HTML) and styles (CSS) in a single file.  
  
To create a Vue 3 app:  

```javascript
// .js
import { createApp } from 'vue'

createApp({
  data() {
    return {
      message: 'Hello Vue!'
    }
  }
}).mount('#app')
```
