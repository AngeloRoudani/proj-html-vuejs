<template>
    <section>
        <!--sezione video-->
        <div class="container">
            <div class="video-title">
                <SectionTitle :smallTitle="'Introduction video'"
                            :mainPart="'Advisory'"
                            :highlightedPart="'Performance'"
                            :paragraph="'Financial executives need to review their strategies, operating models and capabilities so that their areas can generate sound information for better decision making'"
                />
            </div>
            <div class="video-image mt-2">
                <img :src="getImageUrl(videoImage)" alt="video">
                <i class="fa-solid fa-play play-green"></i>
                <i class="fa-solid fa-play play-second"></i>
            </div>
        </div>

    </section>

    <section id="stats">
        <!--sezione stats azienda-->
        <div class="container">
            <h5>What are we doing</h5>
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
                <h5>Our business area</h5>
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
                <SectionTitle :smallTitle="'We like what we do'"
                                :lastPart="'of Experts'"
                                :highlightedPart="'Team'"
                                :paragraph="'Ethics and integrity are the bases on which our professionals build their careers. The are fundamentals that become daily attitudes.'
                "/>
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

    <section id="news">
        <!--sezione delle news-->
        <div class="container">
            <div class="news-title">
                <div class="title-wrapper">
                    <SectionTitle :smallTitle="'Our editorial content'"
                                    :mainPart="'Latest'"
                                    :highlightedPart="'News'"
                                    :paragraph="'Every week we publish content about what is best in the business world'"
                        />
                </div>
                <span class="btn-1">see all</span>
            </div>
            <article class="articles">
                <div v-for="(element,index) in article" class="article" :key="index">
                    <img :src="getImageUrl(element.image)" alt="immagine articolo">
                    <h3>{{ element.title }}</h3>
                </div>
            </article>

        </div>
    </section>
</template>

<script>
import MyServiceCard from './MyServiceCard.vue';
import MyTeamCard from './MyTeamCard.vue';
import SectionTitle from './SectionTitle.vue';

    export default {
        name: 'MyMain',
        components : {
            MyServiceCard,
            MyTeamCard,
            SectionTitle
        },
        data () {
            return {
                videoImage: 'video-1.jpg',
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
                ],
                article: [
                    {
                        image: 'news-1.jpg',
                        title: 'Increasing creativity is possible for everyone'
                    },
                    {
                        image: 'news-2.jpg',
                        title: 'Because market research is part of the business plan'
                    },
                    {
                        image: 'news-3.jpg',
                        title: 'Working from home is now a trend'
                    }
                ]
            }
        },
        methods: {
            getImageUrl(name) {
                return new URL(`../assets/${name}`, import.meta.url).href;
            }
        }
    }

</script>

<style lang="scss" scoped>
 @use '../styles/partials/mainStyle' as *;


</style>
