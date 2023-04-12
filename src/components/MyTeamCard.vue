<template>
    <div class="member-card">
        <img :src="getImageUrl(teamImage)" alt="member photo" class="photo">
        <div>
            <h4>{{ teamName }}</h4>
            <h6>{{ teamRole }}</h6>
            <div>
                <span><i class="fa-brands fa-facebook-f"></i></span>
                <span><i class="fa-brands fa-twitter"></i></span>
                <span><i class="fa-brands fa-linkedin-in"></i></span>
            </div>
        </div>
    </div>

</template>

<script>

    export default {
        name: 'MyTeamCard',
        props: {
            teamImage: String,
            teamName: String,
            teamRole: String
        },
        methods: {
            getImageUrl(path) {
                return new URL(`../assets/${path}`, import.meta.url).href;
            }
        }
    }

</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    .member-card {
        display: flex;

    }
    .photo {
        width: 80px;
        height: 100px;
        border-radius: 5px;
    }

    

</style>