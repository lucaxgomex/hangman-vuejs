<template>
  <div id="app-container">
    <div id="app-home">
      <h1>Welcome to the Hangman Game!</h1>
      <section v-if="definedScreen === 'start'" id="start">
        <Form v-if="step === 'word'" title="Define some word" button="Next" :action="setWord"/>
        <Form v-if="step === 'hint'" title="Define a hint" button="Start Game" :action="setHint"/>
      </section>
      <section v-if="definedScreen === 'game'" id="game">
        <!-- game component -->
        <Game
          :errors="errors"
          :word="word"
          :hint="hint"/>
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
      errors: 0
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
    height: 30%;
  }
}
</style>
