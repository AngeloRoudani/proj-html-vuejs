<template>
    <div class="card">
        <div class="icons">
            <i :class="image" class="icon"></i>
            <i class="fa-solid fa-arrow-right"></i>
        </div>
        <h3>{{ title }}</h3>
        <p>{{ info }}</p>
    </div>
</template>

<script>

    export default {
        name: 'MyServiceCard',
        props: {
            image: String,
            title: String,
            info: String
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
        color: $text-secondary;
        margin-bottom: 1rem;
    }

    .icon {
        font-size: 30px;
    }

    .fa-arrow-right {
        position: relative;
        left: 200px;
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