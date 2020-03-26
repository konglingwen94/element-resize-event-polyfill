# element-resize-event-polyfill

Native event listener polyfill to capture element size changes

## Live Demo 
>https://konglingwen94.github.io/element-resize-event-polyfill/dist/demo.html

## Install

```bash
npm install element-resize-event-polyfill --save-dev
```

### Usage

Example in es6

```javascript
import 'element-resize-event-polyfill'

const elm = document.getElementById('#elm')

elm.addEventListener('resize', handler)
```

Example in browser

```HTML

<head>
  <script src="element-resize-event-polyfill.umd.min.js"></script>
</head>

<body>
  <div id="elm">My size changes can be captured</div>
</body>

<script>
  const elm=document.getElementById("elm")

  // case one
  elm.addEventListener("resize",function(e){
    // Your logic
  })

  // case two
  elm.onresize=function(e){
    // Your logic
  }
</script>


```

Example in vue

```HTML

<template>
  <div v-on:resize="handlerResize"></div>
</template>

<script>
export default {
  methods:{
    handlerResize(e){
      // Your code
    }
  }
}
</script>
```

> Example in cdn

```HTML
<script src="https://unpkg.com/element-resize-event-polyfill@1.0.5/dist/element-resize-event-polyfill.umd.min.js"></script>

<div class="container" id="container">
</div>

<script>
  const elm = document.getElementById('container')

  elm.addEventListener('resize', function(e) {
    // Your code
  })

</script>

