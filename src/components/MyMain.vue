<template>
    <section>
        <div class="container">
            <h6>Introduction video</h6>
            <h1 class="mt-2">Advisory <span class="highlighted">Performance</span></h1>
            <p class="mt-2">Financial executives need to review their strategies, operating models and capabilities so that their areas can generate sound information for better decision making</p>
            <div class="video-image mt-2">
                <img :src="getImageUrl()" alt="video">
                <i class="fa-solid fa-play play-green"></i>
                <i class="fa-solid fa-play play-second"></i>
            </div>
        </div>
    </section>
    <section>
        
    </section>
    <section>
        
    </section>
</template>

<script>

    export default {
        name: 'MyMain',
        data () {
            return {

            }
        },
        methods: {
            getImageUrl() {
                return new URL(`../assets/video-1.jpg`, import.meta.url).href;
            }
        }
    }

</script>

<style lang="scss" scoped>
 @use '../styles/partials/variables' as *;

/*utilities*/

.mt-2 {
    margin-top: 2rem;
}
/*video section*/
.container {
    max-width: 1170px;
    margin: auto;
    padding: 5rem;
    text-align: center;
}

h6 {
    color: $bg-primary;
    text-transform: uppercase;
    font-weight: bold;
}

h1 {
    font-weight: 900;
    font-size: 35px;
    .highlighted {
        display: inline-block;
        padding: .2rem;
        background-color: $bg-secondary;
        color: $bg-primary;
    }
}

p {
    color: $second-grey;
    max-width: 70%;
    margin: auto;
    text-align: center;
    font-size: 14px;
}

.video-image {
    max-width: 80%;
    margin: auto;
    margin-top: 2rem;
    position: relative;
    img {
        width: 100%;
    }
}
.play-green {
    font-size: 60px;
    color: $bg-primary;
    position: absolute;
    left: 47%;
    bottom: 45%;
}

.play-second {
    font-size: 60px;
    color: $play-color;
    position: absolute;
    left: 47%;
    bottom: 43%;
}




</style>
