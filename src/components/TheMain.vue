<template>
    <section class="top">
        <div class="container">
            <div class="card_list">
                <div v-for="(element, index) in Cards" class="card" :key="index">
                    <CardProduct :Photo="element.thumb" :NameComic="element.series" />
                </div>
            </div>
        </div>
        
    </section>
    <section class="bottom">
        <div class="bottom_bg">

        </div>
    </section>
</template>

<script>
    import CardProduct from './CardProduct.vue';

    export default {
        name: 'TheMain',

        components: {
            CardProduct
        },
        props: {
            Cards: Array
        }
        
    }
</script>

<style scoped lang="scss">

@use '../style/partials/variables' as *;
    .top {
        background-color: #1c1c1c;
        
    }
    .container {
        width: 1170px;
        margin: auto;
    }

    .card_list {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }

    .card {
        width: calc((100% / 6) - 1rem);
        margin: 2rem 0.5rem;
    
    }

    .bottom {
        height: 120px;
        background-color: $color-primary;
    }
</style>