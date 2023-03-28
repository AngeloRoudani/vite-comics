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
            <div v-for="(element, index) in utilities" class="mini_card" :key="index">
                <img class="photo" :src="getImageUrl(element.address)" :alt="element.type"/>
                <div class="description">{{ element.type }}</div>
            </div>
        </div>
    </section>
</template>

<script>
    import CardProduct from './CardProduct.vue';

    export default {
        name: 'TheMain',
        data () {
            return {
                utilities: [ 
                        {
                            address: 'buy-comics-digital-comics.png',
                            type: 'Digital Comics'
                        },
                        {
                            address: 'buy-comics-merchandise.png',
                            type: 'Dc merchandise'
                        },
                        {
                            address: 'buy-comics-shop-locator.png',
                            type: 'subscription'
                        },
                        {
                            address: 'buy-comics-subscriptions.png',
                            type: 'comic shop locator'
                        },
                        {
                            address: 'buy-dc-power-visa.svg',
                            type: 'dc power visa'
                        },
                    
                        ]
            }
        },
        components: {
            CardProduct
        },
        props: {
            Cards: Array
            
        },
        methods: {
        getImageUrl(name) {
            return new URL(`../assets/${name}`, import.meta.url).href;
        }
    }
        
    }
</script>

<style scoped lang="scss">
@use '../style/partials/mixins.scss';
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

    .bottom_bg {
        height: 100%;
        @include mixins.flex-center;
        color: $text-secondary;
        
    }

    .mini_card {
        width: calc((100% / 5) - 2rem);
        display: flex;
        align-items: center;
    }
    img {
        width: 40px;
    }
    .description {
        display: inline;
        font-size: 14px;
        text-transform: uppercase;
        font-weight: bold;
        padding-left: 0.5rem;
    }
</style>