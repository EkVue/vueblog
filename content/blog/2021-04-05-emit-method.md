---
title: vue emit method
date: 05-04-2021
category: VueJs
---

v-on directive captures the child components events that is emitted by $emit


Child component triggers clicked event:
```js
export default {
  methods: {
    onClickButton (event) {
      this.$emit('clicked', 'someValue')
    }
  }
}
```

Parent component receive clicked event:
```html
<div>
  <child @clicked="onClickChild"></child>
</div>

```

```js
export default {
  methods: {
    onClickChild (value) {
      console.log(value) // someValue
    }
  }
}
```

