<template>
  <div id="app-container">
    <div id="app-home">
      <h1>Welcome to the Hangman Game!</h1>
      <section v-if="definedScreen === 'start'" id="start">
        <Form v-if="step === 'word'" title="Define some word" button="Next" :action="setWord"/>
        <Form v-if="step === 'tip'" title="Define a tip" button="Start Game"/>
      </section>
      <section v-if="definedScreen === 'game'" id="game">
        Game
      </section>
      <Footer/>
    </div>
  </div>
</template>

<script>
import '@/css/global.css'
import Form from '@/components/Form.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  data() {
    return {
      definedScreen: 'start',
      step: 'word'
    }
  },
  components: {
    Form, Footer
  },
  methods: {
    setWord: function(word) {
      window.alert(`Debug Mode On: ${word}`)
    }
  }
}
</script>

<style>

#app-home {
  width: 100%;
  height: 70%;
  position: absolute;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
