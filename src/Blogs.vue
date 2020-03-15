<template>
    <div id='Blogs'>
        <h1>{{ blogTitle }}</h1>
        <button @click='changeTitle()'>Change Title</button>
    </div>
</template>

<script>
export default {
    name: 'Blogs',
    data(){
       return {
           blogTitle: 'Blog Title'
       }
    },

    methods: {
        changeTitle(){
            this.blogTitle = 'New Blog Title'
        }
    },

    beforeCreate(){
        alert('beforeCreate hook!')
    },

    created(){
        alert('Created Hook!')
    },

    beforeUpdate(){
        alert('beforeUpdate hook!')
    },

    updated(){
        alert('updated hook!')
    }
}
</script>

<style scoped>

</style>