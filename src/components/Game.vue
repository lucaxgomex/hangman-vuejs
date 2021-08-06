<template>
  <div class="game">
    <Stickman
      :errors="errors"/>

    <Word
      :word="word"
      :hint="hint"/>
  </div>
</template>

<script>
import Stickman from './Stickman'
import Word from './Word'

export default {
  name: 'Game',
  components: {
    Stickman, Word
  },
  props: {
    errors: Number,
    word: String,
    hint: String
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
.game {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
</style>
