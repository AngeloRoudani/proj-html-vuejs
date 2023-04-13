<template>
    <form id="message">
        <div class="with-icon">
            <input class="input-text-icon" type="text" placeholder="Name">
            <img :src="getImageUrl()" alt="name" class="little-icon">
        </div>
        <input class="input-text" type="email" placeholder="Email">
        <input class="input-text" type="text" placeholder="Phone">
        <div class="with-icon">
            <input class="input-text-icon" type="text" placeholder="More Info">
            <i class="fa-solid fa-angle-down little-icon"></i>
        </div>
        <textarea class="input-textarea" type="text" rows="5" cols="50" form="message">Message</textarea>
    </form>

</template>

<script>

    export default {
        name: 'FormArea',
        methods: {
            getImageUrl() {
                return new URL(`../assets/image (1).png`, import.meta.url).href;
            }
        }
    }

</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

.with-icon {
    display: inline-block;
    width: 47%;
    height: 36px;
    margin: 0 15px 15px 0;
    position: relative;
}

.input-text {
    width: 47%;
    display: inline-block;
    padding: 10px;
    margin: 0 15px 15px 0;
    background-color: $form-grey;
    border: none;
    border-radius: 3px;
    color: $second-grey;
    outline: none;
}

.input-text-icon {
    width: 100%;
    height: 36px;
    display: inline-block;
    padding: 10px;
    background-color: $form-grey;
    border: none;
    border-radius: 3px;
    color: $second-grey;
    outline: none;
}
.input-textarea {
    width: 96.5%;
    display: block;
    padding: 10px;
    background-color: $form-grey;
    border: none;
    border-radius: 3px;
    color: $second-grey;
    resize: none;
    outline: none;
}

textarea:focus {
    border-color: solid 2px $bg-secondary;
}

.little-icon {
    position: absolute;
    right: 7px;
    top: 10px;
    color: $second-grey;
}

    

</style>