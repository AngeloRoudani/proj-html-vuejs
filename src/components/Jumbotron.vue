<template>
    <div class="bg-jumbo">
        <div class="container-jumbo">
            <div class="navbar">
                <img :src="getImageUrl()" alt="logo" class="logo">
                <ul>
                    <li v-for="(element, index) in navElement" class="list-element" :key="index">{{ element }}</li>
                    <li><i class="fa-regular fa-user"></i></li>
                    <li class="btn-1">Get in touch</li>
                </ul>
            </div>
            <div class="title">
                <h1 class="m-top-2">Financial Risk</h1>
                <p class="m-top-2">The right outcomes depend on continuous rigor in governance, models and processes across the finance function</p>
                <div class="m-top-2">
                    <span class="btn-1">Get In touch</span>
                    <span class="btn-2">Read More</span>
                </div>
            </div>
        </div>
    </div>

</template>

<script>

    export default {
        data () {
            return {
                navElement: [
                    'home',
                    'About',
                    'services',
                    'team',
                    'blog'
                ]
            }
        },
        name: 'Jumbotron',
        methods: {
            getImageUrl() {
                return new URL(`../assets/NexGen-Logo-transparrent.png`, import.meta.url).href;
            }
        }
    }

</script>

<style lang="scss" scoped>
 @use '../styles/partials/variables' as *;
 @use '../styles/partials/btn';

.bg-jumbo {
    background-image: url('../assets/bg-2.jpg');
    height: calc(100vh - 40px);
}

.container-jumbo {
    width: 1170px;
    height: 100%;
    margin: auto;
    color: $first-color;
}

.navbar {
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

ul {
    width: 60%;
    list-style: none;
    text-align: right;
    li {
        display: inline-block;
        text-transform: uppercase;
        margin-left: 2rem;
    }
}

.logo {
    width: 150px;
}

.title {
    height: 80%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
.m-top-2 {
    margin-top: 2rem;
} 
.btn-2 {
    margin-left: 1rem;
}

h1 {
    font-size: 3.5rem;
    font-weight: 900;
}

p {
    width: 700px;
    text-align: center;
}



</style>