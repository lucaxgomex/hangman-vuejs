<template>
  <header id="display-button">
    <button :class="addClass" name="global">{{ description }}</button>
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
