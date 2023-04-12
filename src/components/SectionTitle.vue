<template>
    <h5>{{ smallTitle }}</h5>
    <h1 class="mt-2 stats-title">{{ mainPart }} <span class="highlighted">{{ highlightedPart }}</span> {{ lastPart }}</h1>
    <p class="mt-2">{{ paragraph }}</p>

</template>

<script>

    export default {
        name: 'SectionTitle',
        props: {
            smallTitle: String,
            mainPart: String,
            highlightedPart: String,
            paragraph: String,
            lastPart: String
        }
    }

</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
.mt-2 {
margin-top: 2rem;
}

h5 {
    color: $text-secondary;
    text-transform: uppercase;
    font-weight: bold;
}

h1 {
    font-weight: 900;
    font-size: 35px;
}

.highlighted {
    display: inline-block;
    padding: .2rem;
    background-color: $bg-secondary;
    color: $bg-primary;
}

p {
    color: $second-grey;
    font-size: 14px;
    display: inline-block;
}

    

</style>