<template>
    <div class="foot_bg">
        <div class="container">
            <div class="foot_links">
                <ul class="first">
                    <h3>DC COMICS</h3>
                    <li v-for="element in comics">{{element}}</li>
                </ul>
                <ul class="third">
                    <h3>DC</h3>
                    <li v-for="element in dc">{{ element }}</li>
                </ul>
                <ul class="fourth">
                    <h3>SITES</h3>
                    <li v-for="element in sites">{{ element }}</li>
                </ul>
                <ul class="second">
                    <h3>SHOP</h3>
                    <li v-for="element in shop">{{ element }}</li>
                </ul>
            </div>
            
                <img class="foot_logo" src="../assets/dc-logo-bg.png" alt="logo dc">
            
        </div>
    </div>

</template>

<script>
    export default {
        name: 'TheFooterTop',
        data () {
            return {
            comics: ['Characters','Comics', 'Movies', 'TV', 'Games', 'Videos','News'],
            shop: ['Shop DC', 'Shop DC Collectibles'],
            dc:[ 'Terms Of Use','Privacy policy', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certicates', 'Ratings', 'Shop Help', 'Contact us'],
            sites: ['DC', 'MAD Magazine','DC Kids', 'DC Universe', 'DC Power Visa']
            }
        }
    }
</script>

<style scoped lang="scss">
    .foot_bg {
        height: 40vh;
        background-image: url('../assets/footer-bg.jpg');
        display: flex;
    }

    .container {
        width: 1170px;
        height: 100%;
        margin: auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .foot_links {
        width: 30%;
        display: flex;
        flex-wrap: wrap;
        ul {
            width: calc(100% / 3);
            list-style: none;
        }
    }

    h3 {
        color: #fff;
    }

    li {
        color: #959595;
        font-size: 10px;
        li:hover {
            color: #fff;
        }
    }

    .foot_logo {
        width: 40%;
        height: 100%;
        object-fit: cover;
    }


</style>