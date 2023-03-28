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
    width: 100%;
}

img {
    width: 100%;
    height: 200px;
    object-fit: fill;
    
}

.name {
    color: white;
    text-transform: uppercase;
    font-weight: bold;
    padding-top: 1rem;
    font-size: 14px;
}



</style>