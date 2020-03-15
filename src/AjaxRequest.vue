<template>
    <div id='AjaxRequest'>
        <h1>{{title}}</h1>
        <ul>
            <li v-for='post in posts' :key="post.id">
                {{post.id}}. <br/>
                <h3>{{post.title}}</h3>
                <p>{{post.body}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'AjaxRequest',
    data(){
        return {
            title: 'Making Ajax Request',
            posts: []
        }
    },

    created(){
        axios.get('https://jsonplaceholder.typicode.com/posts').then(response => {
            this.posts = response.data
        }).catch(err => {
            console.log(err)
        })
    }
}
</script>

<style scoped>
ul {
    list-style: none;
}
</style>