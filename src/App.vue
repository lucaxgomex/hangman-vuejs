<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">
        <Header class="button-class" description="Home"/>
      </router-link>
      <router-link to="/about">
        <Header class="button-class" description="About Me"/>
      </router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  },
  methods: {
    update: function() {
      window.location.reload()
    }
  }
}
</script>

<style>
#nav {
  display: flex;
  flex-direction: row;
  margin: 50px;
  padding: 20px;
  justify-content: center;
}

.button-class {
  width: 100px;
}

/**
#app {
  top: 5px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

*/
/*
#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 15px;
  margin: 15px;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
*/
</style>
