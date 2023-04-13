<template>
    <div class="card">
        <div class="icons">
            <i :class="image" class="icon" v-bind:class="iconChange==true?'newcolor':''"></i>
            <i class="fa-solid fa-arrow-right" 
                v-on:mouseover="mouseover" v-on:mouseleave="mouseleave"
                :class="change==true?'arrow-hover':''"></i>
        </div>
        <h3>{{ title }}</h3>
        <p>{{ info }}</p>
    </div>
</template>

<script>

    export default {
        name: 'MyServiceCard',
        data () {
            return {
                change: false,
                iconChange: false
            }
        },
        props: {
            image: String,
            title: String,
            info: String
        },
        methods: {
            mouseover: function () {
                this.change = true;
                this.iconChange = true;
            },
            mouseleave: function () {
                this.change = false;
                this.iconChange = false;
            },
        }
    }

</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    .card {
        padding: 2rem;
        display: flex;
        flex-direction: column;
    }
    .icons {
        margin-bottom: 1rem;
    }
    .icon {
        font-size: 30px;
        color: $text-secondary;
    }

    .fa-arrow-right {
        position: relative;
        left: 200px;
        color: $text-secondary;
        cursor: pointer;
    }

    .arrow-hover {
        display: inline-block;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        padding: 2px 0 0 3px;
        background-color: $text-secondary;
        color: $first-color;
    }
    .newcolor {
        color: $first-color;
    }

    h3 {
        font-weight: 800;
        color: $first-color;
    }

    p {
        color: $text-third;
        margin-top: 1.5rem;
    }

    

</style>