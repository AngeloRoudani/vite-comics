<template>
    <div class="container">
        <img :src="Photo" class="photo">
        <div class="name">{{ NameComic }}</div>
    </div>

</template>

<script>
    export default {
        name: "CardProduct",

        props: {
            Photo: String,
            NameComic: String
        }

    }
</script>

<style scoped lang="scss">

.container {
    width: calc((100% / 6) - 1rem);
    
}

img {
    width: 100%;
}


</style>