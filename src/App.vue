
<template>

        <TheHeader/>
    <main>
        <Jumbotron/>
        <TheMain :Cards="product"/>
    </main>
    <footer>
        <TheFooterTop :Books="comics" :Buy="shop" :House="dc" :Web="sites"/>
        <TheFooterBottom/>
    </footer>

</template>

<script>

    import TheHeader from './components/TheHeader.vue';
    import TheMain from './components/TheMain.vue'
    import TheFooterTop from './components/TheFooterTop.vue';
    import TheFooterBottom from './components/TheFooterBottom.vue';
    import Jumbotron from './components/Jumbotron.vue';

    export default {

        data () {
            return {
                product: [
                            {
                                "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                                "price": "$19.99",
                                "series": "Action Comics",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                                "price": "$3.99",
                                "series": "American Vampire 1976",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                                "price": "$16.99",
                                "series": "Aquaman",
                                "type": "graphic novel"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                                "price": "$2.99",
                                "series": "Batgirl",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640", 
                                "price": "$3.99",
                                "series": "Batman",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                                "price": "$2.99",
                                "series": "Batman Beyond",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                                "price": "$3.99",
                                "series": "Batman/Superman",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                                "price": "$4.99",
                                "series": "Batman/Superman Annual",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                                "price": "$5.99",
                                "series": "Batman: The Joker War Zone",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                                "price": "$6.99",
                                "series": "Batman: Three Jokers",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                                "price": "$4.99",
                                "series": "Batman: White Knight Presents: Harley Quinn",
                                "type": "comic book"
                            },
                            {
                                "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                                "price": "$16.99",
                                "series": "Catwoman",
                                "type": "graphic novel"
                            }
                            ],
                comics: ['Characters','Comics', 'Movies', 'TV', 'Games', 'Videos','News'],
                shop: ['Shop DC', 'Shop DC Collectibles'],
                dc:[ 'Terms Of Use','Privacy policy', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certicates', 'Ratings', 'Shop Help', 'Contact us'],
                sites: ['DC', 'MAD Magazine','DC Kids', 'DC Universe', 'DC Power Visa'],
                
            }
        },

        components : {
            TheHeader,
            TheFooterTop,
            TheMain,
            TheFooterBottom,
            Jumbotron
        }
    }
</script>

<style lang="scss">
    @use './style/general.scss';
</style>
