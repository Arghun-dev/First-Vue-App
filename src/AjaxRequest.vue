<template>
    <div id='AjaxRequest'>
        <h1>{{title}}</h1>
        <input type="text" v-model="searchItem">
        <ul>
            <li v-for='post in filteredPosts' :key="post.id">
                {{post.id}}. <br/>
                <h3>{{post.title}}</h3>
                <p>{{post.body | snippet}}</p>
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
            searchItem: '',
            posts: []
        }
    },

    computed: {
        filteredPosts(){
            return this.posts.filter(post => {
                return post.title.match(this.searchItem)
            })
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