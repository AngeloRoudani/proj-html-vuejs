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

    <section id="team">
        <!--sezione del Team-->
        <div class="container">
            <div class="main-team">
                <h6>We like what we do</h6>
                <h1 class="mt-2"><span class="highlighted">Team</span> of Experts</h1>
                <p class="mt-2">Ethics and integrity are the bases on which our professionals build their careers. The are fundamentals tha become daily attitudes.</p>
                <div class="team-list">
                    <div v-for="(member, index) in team" class="team-member" :key="index">
                        <MyTeamCard 
                            :teamImage="member.image" 
                            :teamRole="member.role"  
                            :teamName="member.name"
                        />
                    </div>
                </div>
            </div>
            <div class="president-speech">
                <h3>President Speech</h3>
                <div>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor quas quasi ratione est iusto quae assumenda necessitatibus magni non!</div>
                <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt eaque, blanditiis id at dignissimos architecto exercitationem nostrum doloribus placeat, voluptatibus unde.</div> 
                <div> Consequuntur sunt perspiciatis nam incidunt distinctio ipsum, illum recusandae.</div>
                <h5>T.Johnson</h5>
                <i class="fa-solid fa-quote-right"></i>
            </div>

        </div>

    </section>
</template>

<script>
import MyServiceCard from './MyServiceCard.vue';
import MyTeamCard from './MyTeamCard.vue';

    export default {
        name: 'MyMain',
        components : {
            MyServiceCard,
            MyTeamCard
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
                ],
                team: [
                    {
                        name: 'David Cooper',
                        role: 'cto & co-founder',
                        image: 'team-1.jpg'
                    },
                    {
                        name: 'Oliver Jones',
                        role: 'chief procurement',
                        image: 'team-3.jpg'
                    },
                    {
                        name: 'Emma Lopez',
                        role: 'chief marketing',
                        image: 'team-2.jpg'
                    },
                    {
                        name: 'T. Johnson',
                        role: 'ceo & president',
                        image: 'team-4.jpg'
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
 @use '../styles/partials/mainStyle' as *;


</style>
