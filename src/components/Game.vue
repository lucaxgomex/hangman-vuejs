<template>
  <div class="game">
    <Stickman
      :errors="errors"/>

    <Word
      :word="word"
      :hint="hint"
      :validation="validation"
      :step="step"/>

    <Keyboard
      v-if="step === 'game'"
      :letters="letters"
      :validation="validation"
      :play="play"/>

    <End
      v-if="step !== 'game'"
      :step="step"
      :message="step === 'winner' ? 'Congulations' : 'Sorry, you lost'"
      :playAgain="playAgain"/>
  </div>
</template>

<script>
import Stickman from './Stickman'
import Word from './Word'
import Keyboard from './Keyboard'
import End from './End'

export default {
  name: 'Game',
  components: {
    Stickman, Word, Keyboard, End
  },
  props: {
    errors: Number,
    word: String,
    hint: String,
    validation: Function,
    step: String,
    letters: Array,
    play: Function,
    playAgain: Function
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
