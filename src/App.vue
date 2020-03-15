<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <h2>Navbar Component</h2>
    <Navbar />
    <h1>All friends</h1>
    <AllFriends :friends='friends' @delete='deleteFriend' />
    <h1>Online friends</h1>
    <OnlineFriends :friends='friends' />
    <Blogs />
  </div>
</template>

<script>
import Navbar from './Navbar';
import AllFriends from './AllFriends';
import OnlineFriends from './OnlineFriends';
import Blogs from './Blogs';

export default {
  name: 'app',
  components: {
    Navbar,
    AllFriends,
    OnlineFriends,
    Blogs
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
  },

  methods: {
    deleteFriend(payload){
      this.friends = this.friends.filter(friend => friend.name !== payload.name)
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
