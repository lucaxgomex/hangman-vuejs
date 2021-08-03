<template>
  <div class="about">
    <img src="../assets/Profile.jpg" alt="My profile picture">
    <section id="about-me">
      I like data
    </section>
    <Footer/>
  </div>
</template>

<script>
import Footer from '../components/Footer.vue'

export default {
  components: {
    Footer
  }
}
</script>

<style>
img {
  width: 180px;
  height: 250px;
  border-radius: 50%;
  display: flex;
}

#about-me {
  border-right: 5px solid var(--color-text-title);
  border-bottom: 5px solid var(--color-text-title);
  width: 100px;
}
</style>
