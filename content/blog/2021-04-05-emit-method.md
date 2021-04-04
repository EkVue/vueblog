---
title: Seattle
date: Sunday May 6th, 2018
thumbnail: /images/uploads/seattle.jpg
category: delphi
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
