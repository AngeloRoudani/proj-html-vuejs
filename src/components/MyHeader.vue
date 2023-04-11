<template>
    <div class="container_top">
        <div class="infobar">

            <div class="open_hours">
                <span><i class="fa-solid fa-clock"></i></span>
                <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
            </div>

            <div class="contacts">
                <div class="phone_number">
                    <span><i class="fa-solid fa-phone"></i></span>
                    <span>+1(305) 1234-5678</span>
                </div>
                <div class="email">
                    <span><i class="fa-solid fa-envelope"></i></span>
                    <span>hello@example.com</span>
                </div>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin-in"></i>
            </div>

        </div>
    </div>
</template>

<script>

    export default {
        name: 'MyHeader'
    }

</script>

<style scoped lang="scss">
 @use '../styles/partials/variables' as *;

.container_top {
    height: 40px;
    background-color: #21333e;
}
.infobar {
    height: 100%;
    max-width: 1170px;
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: $first-color;
    font-size: 12px;
}
.contacts {
    width: 40%;
    display: flex;
    justify-content: space-between;
}

i {
    padding-right: .2rem;
}

</style>
