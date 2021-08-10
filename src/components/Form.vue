<template id="">
  <div class="formulary">
    <div class="formulary-title">{{ title }}</div>
    <input class="formulary-input" type="text" v-model="inputValue">
    <button :disabled="inputValue.length === 0" name="global" v-on:click="onSubmit">{{ button }}</button>
  </div>
</template>

<script>
export default {
  name: 'Form',
  props: {
    title: String,
    button: String,
    action: Function
  },
  data() {
    return {
      inputValue: ''
    }
  },
  methods: {
    onSubmit: function() {
      this.action(this.inputValue)
      this.inputValue = ''
    }
  }
}
</script>

<style media="screen">
.formulary {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  justify-content: center;
  margin-top: 20px;
}

.formulary-input {
  padding: 10px 5px;
  border: none;
  margin: 10px 5px;
  text-align: center;
  color: var(--color-text-dark);
  font-size: 15px;
}
</style>
