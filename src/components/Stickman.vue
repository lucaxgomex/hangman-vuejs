<template>
  <div class="stickman-figure">
    <img :src="`https://raw.githubusercontent.com/lucaxgomex/hangman-vuejs/main/src/assets/images/${errors}.svg`" alt="Game assets">
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
