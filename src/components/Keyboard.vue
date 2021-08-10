<template>
  <div class="keyboard">
    <button class="keyboard-buttom"
      v-for="(letter, key) in 'qwertyuiopasdfghjklzxcvbnm'"
      :key="key"
      :disabled="validation(letter)"
      @click="play(letter)">
      {{ letter }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'Keyboard',
  props: {
    letters: Array,
    validation: Function,
    play: Function
  }
}
</script>

<style>
.keyboard {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 85%;
  margin-top: 20px;
}

.keyboard-buttom {
  margin: 5px;
  text-transform: uppercase;
}
</style>
