<template>
    <div class="member-card">
        <img :src="getImageUrl(teamImage)" alt="member photo" class="photo">
        <div class="description">
            <h4>{{ teamName }}</h4>
            <div class="role">{{ teamRole }}</div>
            <div>
                <span class="icon-rounded"><i class="fa-brands fa-facebook-f"></i></span>
                <span class="icon-rounded"><i class="fa-brands fa-twitter"></i></span>
                <span class="icon-rounded"><i class="fa-brands fa-linkedin-in"></i></span>
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

    .role {
        text-transform: uppercase;
        color: $second-grey;
        font-size: 12px;
    }

    .member-card h4, .role {
        margin-bottom: .7rem
    }
    .description {
        margin-left: 1rem;
    }
    .icon-rounded {
        display: inline-block;
        width: 30px;
        height: 30px;
        background-color: $bg-secondary;
        color: $bg-primary;
        border-radius: 50%;
        position: relative;
        margin-right: 5px ;
        i {
            position: relative;
            top:5px;
            left: 8px;
        }
    }

    

</style>