<template>
        <h5>{{ smallTitle2 }}</h5>
        <div class="mt-1 stats-title">{{ mainPart2 }} <span class="highlighted-white">{{ highlightedPart2 }}</span> {{ lastPart2 }}</div>
        <p class="mt-1 p-white">{{ paragraph2 }}</p>

</template>

<script>

    export default {
        name: 'SectionTitle2',
        props: {
            smallTitle2: String,
            mainPart2: String,
            highlightedPart2: String,
            paragraph2: String,
            lastPart2: String
        }
    }

</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
.mt-1 {
margin-top: 1.5rem;
}

h5 {
    color: $text-secondary;
    text-transform: uppercase;
    font-weight: bold;
}

.stats-title {
    font-weight: 900;
    font-size: 35px;
}

.highlighted-white {
    padding: .2rem .3rem;
    background-color: $bg-secondary;
    color: $first-color;
    border-radius: 3px;
}

.p-white {
    color: $first-color;
    font-size: 14px;
    display: inline-block;
}


    

</style>