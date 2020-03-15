<template>
  <div id="app">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      title: 'My first Vue App'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Baloo 2', cursive;
}

h1 {
  color: #444;
  text-align: center;
}
</style>
