---
title: vue emit method
date: 05-04-2021
thumbnail: /images/uploads/vue.png
category: Delphi
---

v-on directive captures the child components events that is emitted by $emit

Child component triggers clicked event:

```
export default {
  methods: {
    onClickButton (event) {
      this.$emit('clicked', 'someValue')
    }
  }
}
```
Parent component receive clicked event:

```
<div>
  <child @clicked="onClickChild"></child>
</div>
export default {
  methods: {
    onClickChild (value) {
      console.log(value) // someValue
    }
  }
}
```
