<template>
    <body>
        <MyHeader />
        <MyMain />
        <MyFooter />
    </body>

</template>

<script>

import MyHeader from './components/Myheader.vue';
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
    @use './styles/general.scss';

</style>
