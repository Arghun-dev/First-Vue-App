<template>
    <div id='all-friends'>
        <div v-for='(friend, index) in friends' :key='index'>
            <span>{{friend.name}}</span>
            <button @click="deleteFriend(friend.name)">x</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AllFriends',
    props: ['friends'],
    data(){
        return {

        }
    },

    methods: {
        deleteFriend(name){
            this.$emit('delete', {name: name})
        }
    } 
}
</script>

<style scoped>

</style>