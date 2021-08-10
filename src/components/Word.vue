<template>
  <div class="word">
    <div class="word-letters">
      <div class="each-letter" v-for="(letter, key) in word" :key="key">
        {{ (validation(letter) || step === 'hanged') ? letter : '' }}
      </div>
    </div>
    <div class="display-hint">
      {{ hint }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Word',
  components: {

  },
  props: {
    word: String,
    hint: String,
    validation: Function,
    step: String
  },
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style>
.word {
  text-transform: uppercase;
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
}

.word-letters {
  display: flex;
  margin-bottom: 20px;
}

.each-letter {
  height: 30px;
  width: 30px;
  margin: 0px 5px;
  border-bottom: 1px solid var(--color-text-light);
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
