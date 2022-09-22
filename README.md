#Build settings
theme: cayman

# Vue Introduction
Introduction to Vue 2 and Vue 3.

# Vue
Data and DOM are linked and everything is reactive.  
__Rectivity__ meas that Vue automatically tracks JavaScript state changes and efficiently updates the DOM when changes happan.
### Directives
Directives are special attributes provided by Vue and they apply special reactive behavior to the rendered DOM.
- __v-bind__ (:)    keeps the referred element up-to-date
- __v-if__          toggles the precence of an element


# Vue 2
> To add Vue framework to the project:
```html
<!-- development version, includes helpful console warnings -->
<script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>

<!-- production version, optimized for size and speed -->
<script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
```
___
> To create a Vue 2 app:
```javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```
With | el: '#app' | the Vue App attaches itself to a single DOM element then fully controls it.  
In the index.html you have to write:  
```html
<script src="main.js"></script>
```

___

# Vue 3
> Vue 3 supports __Single-File Component__, or __SFC__ files (*.vue). It encapsulates the component's logic (Javascript), template (HTML) and styles (CSS) in a single file.
> To create a Vue 3 app:
```javascript
import { createApp } from 'vue'

createApp({
  data() {
    return {
      message: 'Hello Vue!'
    }
  }
}).mount('#app')
```
