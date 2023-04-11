<template>
    <body>
        <MyHeader />
        <MyMain />
        <MyFooter />
    </body>

</template>

<script>

import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyFooter from './components/MyFooter.vue';

export default {

    components: {
        MyHeader,
        MyMain,
        MyFooter
    }
}

</script>

<style lang="scss">
    @use './styles/general.scss' as *;

</style>
