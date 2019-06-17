# qrcode.vue

A Vue.js component for [QRCode](https://en.wikipedia.org/wiki/QR_code).

[![Build Status](https://travis-ci.org/scopewu/qrcode.vue.svg?branch=master)](https://travis-ci.org/scopewu/qrcode.vue)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/scopewu/qrcode.vue/blob/master/LICENSE)

[中文](./README-zh_cn.md)

## install

the `qrcode.vue` component can use in you Vue.js app.

```bash
npm install --save qrcode.vue # yarn add qrcode.vue
```

## Usage

e.g.

```javascript
import Vue from 'vue'
import QrcodeVue from 'qrcode.vue'

new Vue({
  el: '#root',
  data: {
    value: 'https://example.com',
  },
  template: '<qrcode-vue :value="value"></qrcode-vue>',
  components: {
    QrcodeVue,
  },
})
```

Or single-file components with a \*.vue extension:

```html
<template>
  <div>
    <qrcode-vue :value="value" :size="size" level="H"></qrcode-vue>
  </div>
</template>
<script>
  import QrcodeVue from 'qrcode.vue'

  export default {
    data() {
      return {
        value: 'https://example.com',
        size: 300,
      }
    },
    components: {
      QrcodeVue,
    },
  }
</script>
```

## Component props

### value

- Type: `string`
- Default: `''`

The value content of qrcode

### level

- Type: `string`
- Default: `L`

qrcode Error correction level (one of 'L', 'M', 'Q', 'H').

### size

- Type: `number`
- Default: `100`

The size of qrcode element.

### background

- Type: `string`
- Default: `#ffffff`

The background color of qrcode.

### foreground

- Type: `string`
- Default: `#000000`

The foreground color of qrcode.

### class

- Type: `string`
- Default: `''`

The class name of qrcode element. Now `className` is renamed to `class`, Its will expire.

## License

copyright &copy; 2017 @scopewu, license by [MIT](https://github.com/scopewu/qrcode.vue/blob/master/LICENSE)
