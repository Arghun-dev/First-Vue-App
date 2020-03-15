<template>
    <nav>
        <ul>
            <li><a href="">Home</a></li>
            <li><a href="">About</a></li>
            <li><a href="">Contact</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    data(){
        return {

        }
    }
}
</script>

<style>
nav {
    text-align: center;
    border: 1px solid #ccc;
    background-color: #ccc;
}

nav ul {
    display: flex;
    justify-content: flex-end;
    list-style: none;
}

nav ul li {
    margin-left: 4rem;
}
</style>