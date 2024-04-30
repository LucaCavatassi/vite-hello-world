<script>  
    export default {
        data () {
            return {
                image: "copy.png",
            }
        },

        methods: {
            getImagePath(imageName) {
                return new URL (`../assets/${imageName}`, import.meta.url).href
            }
        }
    };
</script>

<template>
    <img :src="getImagePath(image)" alt="">
</template>

<style>
    img {
        display: block;
        margin: 0 auto;
    }
</style>