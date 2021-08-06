<template>
  <div class="stickman-figure">
    <img :src="`https://raw.githubusercontent.com/william-costa/wdev-hangman-game-resources/master/images/hangman/${errors}.svg`" alt="Game images">
  </div>
</template>

<script>
export default {
  name: 'Stickman',
  props: {
    errors: Number
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
.stickman-figure img {
  height: 100px;
}
</style>
