<template>
        <div class="foot-top">
            <div class="container">
                <div class="card-wrapper">
                    <div class="card">
                        <img :src="getImageUrl()" alt="logo" class="logo-photo">
                        
                        <div class="g-text">A Functional HTML Template for Corporate & Business</div>
                        <div class="mt-2">
                            <span class="icon"><i class="fa-solid fa-phone"></i></span>
                            <span class="example-text">+1(305) 1234-5678</span>
                        </div>
                        <div class="mt-1">
                            <span class="icon"><i class="fa-solid fa-envelope"></i></span>
                            <span class="example-text">hello@example.com</span>
                        </div>
                        <div class="mt-1">
                            <span class="icon"><i class="fa-solid fa-location-dot"></i></span>
                            <span class="example-text">Main Avenue, 987</span>
                        </div>
                        
                        <span class="btn-2 mt-1">get in touch</span>
                    </div>

                    <div v-for="(element,index) in footerLinks" class="card-links" :key="index">
                        <h3 class="card-title">{{ element.title }}</h3>
                        <ul class="list mt-2">
                            <li v-for="(link,index) in element.links" :key="index" class="mt-half"><i class="fa-solid fa-angle-right"></i> {{ link }}</li>
                        </ul>

                    </div>
                </div>

            </div>
    </div>
    <div class="foot-bottom">
        <div class="container">
            <div class="bottom-wrapper">
                <div class="left-foot">
                    Enjoy the low price. We are tracking any intention of piracy.
                </div>
                <div class="right-foot">
                    &#169; 2023 NEXGEN is Proudly Powered by <a href="#">Codings</a>.
                </div>
            </div>

        </div>

    </div>

</template>

<script>

    export default {
        name: 'MyFooter',
        data () {
            return {
                footerLinks: [
                    {
                        title: 'About',
                        links: [
                            'The Company',
                            'Institutional',
                            'Social & Events',
                            'Innovation',
                            'Environment',
                            'Technology'
                        ]
                    },
                    {
                        title: 'Services',
                        links: [
                            'Audit & Assurance',
                            'Financial Advisory',
                            'Analytics M&A',
                            'Middle Marketing',
                            'Legal Consulting',
                            'Regulatory Risk'
                        ]
                    },
                    {
                        title: 'Support',
                        links: [
                            'Responsibility',
                            'Terms of Use',
                            'About Cookies',
                            'Privicy Policy',
                            'Accessibilty',
                            'Information'
                        ]
                    }
                ]
            }
        },
        methods: {
            getImageUrl() {
                return new URL(`../assets/NexGen-Logo-transparrent.png`, import.meta.url).href;
            }
        }
    }

</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/btn';
.mt-2 {
    margin-top: 2rem;
}

.mt-half {
    margin-top: 10px;
}

.mt-1 {
    margin-top: 1rem;
}
.container {
    max-width: 1170px;
    margin: auto;
    padding: 0 3rem;
}
.foot-top {
    background-image: url('../assets/bg-7.jpg');
    background-size: cover;
    background-position: center;
}
.card-wrapper {
    display: flex;
    justify-content: space-between;
    gap: 2%;
    color: $form-grey;
    padding: 9rem 0;
}
.card {
    width: calc(100% / 4);
}

.card-links {
    width: calc(100% / 4 );
    padding: 2.5rem;
    background-color: $grey-transparrent;
    border-radius: 10px;
}
.icon {
    display: inline-block;
    margin-right: 5px ;
    i {
        color: $bg-third;
    }

}
.logo-photo {
    width: 150px;
}

.btn-2 {
    display: inline-block;
}
.list {
    list-style: none;
}

.card-title {
    font-weight: 900;
}
.foot-bottom {
    background-color: $first-black;
}
.bottom-wrapper {
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: $first-color;
    font-size: 14px;
    a {
        text-decoration: none;
        color: $bg-primary;
    }
}



    

</style>
