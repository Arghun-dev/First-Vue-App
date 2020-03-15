<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <h2>Navbar Component</h2>
    <Navbar />
  </div>
</template>

<script>
import Navbar from './Navbar';

export default {
  name: 'app',
  components: {
    Navbar
  },
  data () {
    return {
      title: 'My first Vue App'
    }
  }
}
</script>

<style scoped>
#app {
  font-family: 'Baloo 2', cursive;
}

h1 {
  color: #444;
  text-align: center;
}
</style>
