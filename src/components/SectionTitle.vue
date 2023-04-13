<template>
    <div class="version-1">
        <h5>{{ smallTitle }}</h5>
        <div class="mt-1 stats-title">{{ mainPart }} <span class="highlighted"> {{ highlightedPart }}</span> {{ lastPart }}</div>
        <p class="mt-1 p-grey">{{ paragraph }}</p>
    </div>

</template>

<script>

    export default {
        name: 'SectionTitle',
        props: {
            smallTitle: String,
            mainPart: String,
            highlightedPart: String,
            paragraph: String,
            lastPart: String,
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

.highlighted {
    padding: .2rem .3rem;
    background-color: $bg-secondary;
    color: $bg-primary;
    border-radius: 3px;
}

.p-grey {
    color: $second-grey;
    font-size: 14px;
    display: inline-block;
}


</style>