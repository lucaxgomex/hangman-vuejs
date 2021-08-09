<template>
  <div id="about">
    <img src="../assets/Profile.png" alt="My profile picture">
    <section>
      <p id="content">
        I truly believe in the power of technology. Over 2 or 3 years ago I've written my first JavaScript code lines. It was all new to me that days, I must say - even I didn't know a thing about frameworks, frontend developement or software architecture. As time goes by, it was about time to contribute with coding the best way I could, which I did through React in a college project. It was almost one entire year using React and understang its patterns. When I leave the project, I decided to push myself really hard in something great, and Vue.js was this choice. It's the framework I'm focusing now in.
      </p>
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
#about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

img {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  display: flex;
  opacity: 0.5;
  margin: 10px;
}

#about img:hover {
  opacity: inherit;
}

section #content {
  border-top: 1px solid var(--color-text-title);
  border-bottom: 1px solid var(--color-text-title);
  width: 100%;
  padding: 15px;
  text-align: center;
  font-size: 12px;
}
</style>
