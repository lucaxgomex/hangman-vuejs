<template>
  <header id="display-button">
    <button>{{ description }}</button>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    description: String
  }
}
</script>

<style media="screen">
a {
  text-decoration: none;
}
</style>
