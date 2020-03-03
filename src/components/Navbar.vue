<template>
    <nav>
        <h2>Menu</h2>
        <ul>
            <li><router-link :to="{name: 'Home'}">Home</router-link></li>
            <li><router-link :to="{name: 'About'}">About</router-link></li>
        </ul>
        <dir class="d-flex flex-row justify-content-center p-2">
            <button @click="goBack">Go Back</button>
            <button @click="goHome">Go Home</button>            
            <button @click="goForward">Go Forward</button>
        </dir>
        
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            
        }
    },
    methods: {
        goHome(){
            this.$router.push({name: 'Home'})
        },
        goBack(){
            this.$router.go(-1)
        },
        goForward(){
            this.$router.go(1)
        }
    }
}
</script>
<style scoped>
    nav {
        text-align: center;
    }
    nav ul {
        padding: 0;
    }
    nav li {
        margin: 5px;
        list-style-type: none;
        display: inline-block;
    }
    a.router-link-exact-active {
        color: green;
    }
</style>