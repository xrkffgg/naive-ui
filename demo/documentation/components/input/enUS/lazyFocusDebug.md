# Lazy Focus

If you want to focus input element after focus at input wrapper and press enter.

```html
<n-input
  v-model="value"
  @blur="handleBlur"
  @focus="handleFocus"
  @change="handleChange"
  @keyup="handleKeyUp"
  @input="handleInput"
  placeholder="Operate to trigger events"
  :passively-activated="true"
/>
<n-input
  v-model="value"
  type="textarea"
  @blur="handleBlur"
  @focus="handleFocus"
  @change="handleChange"
  @keyup="handleKeyUp"
  @input="handleInput"
  placeholder="Operate to trigger events"
  :passively-activated="true"
/>
<n-input
  pair
  seperator="to"
  v-model="pair"
  @blur="handleBlur"
  @focus="handleFocus"
  :passively-activated="true"
/>
```
```js
export default {
  data() {
    return {
      value: null,
      pair: null
    }
  },
  methods: {
    handleFocus(e) {
      this.$NMessage.info('[Event focus]')
    },
    handleBlur(e) {
      this.$NMessage.info('[Event blur]')
    },
    handleChange(v) {
      this.$NMessage.info('[Event change]: ' + v)
    },
    handleKeyUp(e) {
      this.$NMessage.info('[Event keyup]')
    },
    handleInput(v) {
      this.$NMessage.info('[Event input]: ' + v)
    }
  }
}
```
```css
.n-input {
  margin-bottom: 8px;
}
```