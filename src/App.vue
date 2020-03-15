<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <h2>Navbar Component</h2>
    <Navbar />
    <h1>All friends</h1>
    <AllFriends :friends='friends' />
    <h1>Online friends</h1>
    <OnlineFriends :friends='friends' />
  </div>
</template>

<script>
import Navbar from './Navbar';
import AllFriends from './AllFriends';
import OnlineFriends from './OnlineFriends';

export default {
  name: 'app',
  components: {
    Navbar,
    AllFriends,
    OnlineFriends
  },
  data () {
    return {
      title: 'My first Vue App',
      friends: [
        {name: 'Arghun', online: true},
        {name: 'mammad', online: false},
        {name: 'milad', online: true},
        {name: 'Feyzi', online: false}
      ]
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
