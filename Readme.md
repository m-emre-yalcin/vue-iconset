# vue-iconset

This iconset component will make easier to work with svg icons in your vue project.

## Installation

`npm install vue-iconset`

## Usage

```js
// main.js
let options = {
    icons: {
        icon:"<svg><path>...</svg>"
    }
}

import Vue from 'vue'
import VueIconset from 'vue-iconset'
Vue.use(VueIconset, options)
```

### After configuration you can use it in all templates!

```html
<template>
    <icon name="document" fill="green"/>
</template>
```

## Options

```js
// there are some default icons you can use in 'default-icons.js' file:
["attach", "ban", "camera", "close", "comment", "completed", "confirm", "cursor", "dashboard", "delete", "document", "down-arrow", "download", "edit", "eye", "filter", "flip", "history", "image", "info", "key", "label", "layers", "like", "logout", "mail", "mention", "minus", "more", "new-form", "not-completed", "notification", "ok", "password", "pinned", "plus", "refresh", "settings", "share-link", "star", "trash", "user", "warning"]
```

```js
// default properties:
props: {
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
