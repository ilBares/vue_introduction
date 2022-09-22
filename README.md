# vue_introduction
Introduction to Vue 2 and Vue 3.

#Vue
Data and DOM are linked and everything is reactive.


#Vue 2
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
```js
<script src="main.js"></script>
```

___

#Vue 3
> To create a Vue 3 app:
```
import { createApp } from 'vue'

createApp({
  data() {
    return {
      message: 'Hello Vue!'
    }
  }
}).mount('#app')
```
