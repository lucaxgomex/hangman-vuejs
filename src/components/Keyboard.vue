<template>
  <div class="keyboard">
    <button class="keyboard-button" name="keyboard"
      v-for="(letter, key) in 'abcdefghijklmnopqrstuvw'"
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
  border: 1px solid var(--color-text-light);
  padding: 5px 0px 25px;
}

.keyboard-button {
  margin: 5px;
  text-transform: uppercase;
}
</style>
