<template>
  <header id="display-button">
    <button :class="addClass">{{ description }}</button>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    description: String,
    addClass: String
  }
}
</script>
