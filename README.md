# Vue js
Data and DOM are linked and everything is reactive.  
__Rectivity__ meas that Vue automatically tracks JavaScript state changes and efficiently updates the DOM when changes happan.  
The Vue framework uses Shadow DOM that allows hidden DOM trees to be attached to elements in the regular DOM tree.  

## Directives
Directives are special attributes provided by Vue and they apply special reactive behavior to the rendered DOM.  
Directive structure:
<pre>v-[directive name]:[argument name]</pre>  

#### Main directives:  
- __v-bind__ (:)<pre>keeps the referred element up-to-date</pre>
- __v-if__<pre>toggles the precence of an element</pre>
- __v-show__<pre>show an element only if the condition is true</pre>
- __v-for__<pre>used for displaying a list of items using the data from an Array</pre>
- __v-on__ (@) <pre>attaches event listeners that invoke methods on our Vue instances. It listens for specific events (like "click", "mousemove", ...)</pre>
- __v-model__<pre>it makes two-way binging between element and data</pre>

## Vue Instance
### Options / Data
To access Options you have to write: ```javascript vm.$[option] ```
- __data__ | _Function_ | <pre>Vue will recyrsively convert its properties into getter/setters to make it "reactive".</pre>
- __props__ | _ArrayList<String>_ or _Object_ | <pre>A list of attributes that are exposed to accept data from the parent component.</pre>
With Object-based syntax, you can use following options: _type_, _default_, _required_, _validator_.
- __computed__ <pre>Computed properties to be mixed into Vue instance. Computed property are cached, and only re-computed on reactive dependency changes.</pre>
- __methods__ | [key: String]: Function] | <pre>Methods to be mixed into the Vue instance.</pre>
- __watch__ <pre>An object where keys are expressions to watch and values are the corrisponding callbacks.</pre>

### Options / DOM
- __el__ | _String_ | <pre>Provide the Vue instance an existing DOM element to mount on. If this option is not available at instantiation, the user will have to explicitly call _vm.$mount()_.</pre>
- __template__ | _String_ | <pre>A string template to be used as the markup for the Vue instance. The template will replace the mounted element.</pre>
  
### Options / Lifecycle Hooks
LifeCycle Diagram: https://v2.vuejs.org/images/lifecycle.png
- __beforeCreate__ | _Function_ | <pre>Called synchronously immediately after the instance has been initialized, before data observation and event/watcher setup.</pre>
- __created__ | _Function_ | <pre>Called synchronously after the instance is created (the instance has already finished processing the options).</pre>
- __beforeMount__ | _Function_ |
- __mounted__ | _Function_ |
- __beforeUpdate__ | _Function_ |
- __updated__ | _Function_ |
- __beforeDestroy__ | _Function_ |
- __destroyed__ | _Function_ |
  
## Components
> The components system is an abstraction that allows us to build large-scale applications composed of small and reusable components.
> Vue component model allow us to encapsulate custom content and logic in each component. Vue components are also Vue instances, so accept the same option object.

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
// "vm" stands for "ViewModel" (MVVM pattern)
var vm = new Vue({
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
// .js
// Define a new component called todo-item
Vue.component('todo-item', {
  template: '<li>This is a todo</li>'
})

var app = new Vue(...)
```

### Vue Instance structure:
```javascript
// .js
var vm = new Vue({
  // options
  data() { return ... },
  prop: { ... },
  computed() { return ... },
  methods: {}
})
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



/////// TO REMOVE
si puo aggiungere il file .env per aggiungere variabili di environment (dopo è necessario riavviare il server)
.env.development    -> usato da npm run serve
.env.production     -> usato da npm run build

formato variabile:
VUE_APP_URL_SERVER=www.bares.com


https://ilbares.github.io/vue_introduction/
