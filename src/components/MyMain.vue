<template>
    <section>
        <!--sezione video-->
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

    <section id="stats">
        <!--sezione stats azienda-->
        <div class="container">
            <h6>What are we doing</h6>
            <h1 class="mt-2 stats-title"><span class="highlighted">Results</span> in Numbers</h1>
            <div class="stats-info">
                <div v-for="(element,index) in statsList" class="minicard" :key="index">
                    <div class="number">{{ element.quantity }}</div>
                    <div class="info-name">{{ element.label }}</div>
                </div>
            </div>
        </div>
    </section>
    <section>
        
    </section>
</template>

<script>

    export default {
        name: 'MyMain',
        data () {
            return {
                statsList: [
                    {
                        quantity: 128,
                        label: 'Certifications'
                    },
                    {
                        quantity: 230,
                        label: 'Employees'
                    },
                    {
                        quantity: 517,
                        label: 'Customers'
                    },
                    {
                        quantity: 94,
                        label: 'Coutry Served'
                    }
                ]
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
}
.highlighted {
    display: inline-block;
    padding: .2rem;
    background-color: $bg-secondary;
    color: $bg-primary;
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

/*statistiche azienda*/
#stats {
    background-image: url('../assets/bg-3.jpg');
    background-size: cover;
}

.stats-title {
    color: $first-color;
    span {
        color:$first-color;
    }
}
.stats-info {
    width: 100%;
    display: flex;
    justify-content: space-between;
    margin: 4rem;
}

.minicard {
    width: calc(100%/ 4);
}

.number {
    color: $text-secondary;
    font-size: 40px;
    font-weight: bolder;
}

.info-name {
    color: $first-color;
    text-transform: uppercase;
    font-weight: bolder;
}




</style>
