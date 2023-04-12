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


    <section id="servicies">
        <!--sezione servizi e prodotti-->
        <div class="container">
            <div class="title-wrapper">
                <h6>Our business area</h6>
                <h1 class="mt-2 stats-title">Excellence in <span class="highlighted">Services</span></h1>
                <p class="mt-2 ">We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals.These are some options that you can hire.</p>
                <span class="btn-2">see all</span>
            </div>
            <div class="services-list">
                <div v-for="(element,index) in servicies" class="product" :key="index"> 
                    <MyServiceCard 
                                :image="element.image"
                                :title="element.title"
                                :info="element.info"/>
                </div>
            </div>
        </div>
        
    </section>
</template>

<script>
import MyServiceCard from './MyServiceCard.vue';

    export default {
        name: 'MyMain',
        components : {
            MyServiceCard
        },
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
                ],
                servicies: [
                    {
                        image: 'fa-solid fa-network-wired',
                        title: 'Audit & Assurance',
                        info: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                    },
                    {
                        image: 'fa-solid fa-briefcase',
                        title: 'Financial Advisory',
                        info: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                    },
                    {
                        image: 'fa-solid fa-chart-simple',
                        title: 'Analitics and M&A',
                        info: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                    },
                    {
                        image: 'fa-solid fa-plane',
                        title: 'Middle Marketing',
                        info: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                    },
                    {
                        image: 'fa-solid fa-globe',
                        title: 'Legal consulting',
                        info: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
                    },
                    {
                        image: 'fa-solid fa-inbox',
                        title: 'Regulatory Risk',
                        info: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.'
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
 @use '../styles/partials/btn';

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

#stats .container {
    text-align: center;
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
    margin-top: 4rem;
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
/*servizi e prodotti*/

#servicies {
    background-color: $first-black;
}

#servicies p {
    color: $text-third;
    text-align: left;
    display: inline-block;
}

#servicies .container {
    text-align: left;
    padding: 4rem 0;
}

.title-wrapper {
    width: 91%; 
    margin: auto;
}

#servicies .btn-2 {
    color: $first-color;
    margin-left: 200px;
}
.services-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 2rem auto;
}

.product {
    width: calc((100% / 3.5));
    margin: 1rem;
    background-color: $second-grey;
    border-radius: 5px;
}



</style>
