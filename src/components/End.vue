<template>
  <div class="end">
    <div :class="`end-text ${step}`">
      {{ message }}
    </div>
    <button class="end-button" name="global" @click="playAgain">
      Play Again
    </button>
  </div>
</template>

<script>
export default {
  name: 'End',
  props: {
    step: String,
    message: String,
    playAgain: Function
  }
}
</script>

<style>
.end-text {
  margin: 20px 0px;
  font-size: 24px;
  font-weight: bold;
}

.end-text.hanged {
  color: var(--color-text-error);
}

.end-text.winner {
  color: var(--color-text-success);
}
</style>
