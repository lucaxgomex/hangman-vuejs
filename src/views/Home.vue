<template>
  <div id="app-container">
    <div id="app-home">
      <h1 v-if="definedScreen === 'start'">Welcome to the Hangman Game!</h1>
      <section v-if="definedScreen === 'start'" id="start">
        <Form v-if="step === 'word'" title="Define some word" button="Next" :action="setWord"/>
        <Form v-if="step === 'hint'" title="Define a hint" button="Start Game" :action="setHint"/>
      </section>
      <section v-if="definedScreen === 'game'" id="game">
        <!-- game component -->
        <Game
          :errors="errors"
          :word="word"
          :hint="hint"
          :validation="validation"
          :step="step"
          :letters="letters"
          :play="play"
          :playAgain="playAgain"/>
      </section>
      <Footer/>
    </div>
  </div>
</template>

<script>
import '@/css/global.css'

import Form from '@/components/Form.vue'
import Footer from '@/components/Footer.vue'
import Game from '@/components/Game'

export default {
  name: 'App',
  data() {
    return {
      definedScreen: 'start',
      step: 'word',
      word: '',
      hint: '',
      errors: 0,
      letters: []
    }
  },
  components: {
    Form, Footer, Game
  },
  methods: {
    setWord: function(word) {
      this.word = word
      this.step = 'hint'
    },

    setHint: function(hint) {
      this.hint = hint
      this.step = 'game'
      this.definedScreen = 'game'
    },

    validation: function(letter) {
      return this.letters.find(item => item.toLowerCase() === letter.toLowerCase())
    },

    play: function(letter) {
      //add letter to the letters object
      this.letters.push(letter)

      this.verifyWrong(letter)
    },

    verifyWrong: function(letter) {
      if (this.word.toLowerCase().indexOf(letter.toLowerCase()) >= 0) {
        return this.verifyRight()
      }

      this.errors++

      if (this.errors === 6) {
        this.step = 'hanged'
      }
    },

    verifyRight: function() {
      let unique = [...new Set(this.word.split(''))]

      if (unique.length === (this.letters.length - this.errors)) {
        this.step = 'winner'
      }
    },

    playAgain: function() {
      this.word = ''
      this.hint = ''
      this.errors = 0
      this.letters = 0
      this.definedScreen = 'start'
      this.step = 'word'
    }
  }
}
</script>

<style>
#app-home {
  width: 100%;
  height: 50%;
  position: absolute;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

@media(max-width: 600px) {
  #app-home {
    height: 50%;
  }
}
</style>
