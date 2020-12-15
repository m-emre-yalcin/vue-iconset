# vue-iconset

This iconset component will make easier to work with svg icons on your vue project.

## Installation

`npm install vue-iconset`

## Usage

```js
// main.js
import Vue from 'vue'
import VueIconset from 'vue-iconset'
import icons from 'vue-iconset/icons' // all svg are here (optional)

Vue.component('icon', {
    extends: VueIconset,
    props: {
        icons: icons, // you can extend this object or use your own icons object
        // you can set default values here
        // height: 30px,
        // width: 30px,
        // fill: 'white'
        // .
        // .
        // .
    }
})
```

### After configuration you can use it in all templates!
```html
<template>
    <icon name="document" fill="green"/>
</template>
```

## Options

```js
// there are some default icons you can use in 'icons.js' file:
["attach", "ban", "camera", "close", "comment", "completed", "confirm", "cursor", "dashboard", "delete", "document", "down-arrow", "download", "edit", "eye", "filter", "flip", "history", "image", "info", "key", "label", "layers", "like", "logout", "mail", "mention", "minus", "more", "new-form", "not-completed", "notification", "ok", "password", "pinned", "plus", "refresh", "settings", "share-link", "star", "trash", "user", "warning"]
```

```js
// vue-iconset props:
props: {
    icons: {
        type: Object,
        default: {}
    },
    name: {
        type: String,
        default: 'star'
    },
    fill: {
        type: String,
        default: "#333"
    },
    width: {
        type: String,
        default: "20px"
    },
    height: {
        type: String,
        default: "20px"
    },
    viewBox:{
        type: String,
    },
    rotate:{
        type: String,
        default: "0deg"
    },
}
```

```js
// example icons.js object:
export default {
    attach: '<svg xmlns="http://www.w3.org/2000/sv...',
    ban: '<svg viewBox="0 -256 1792 1792"...',
    camera: '<svg version="1.1" id="Layer_1"..."',
    // .
    // .
    // .
    // .

```
