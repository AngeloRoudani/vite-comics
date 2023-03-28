<template>
    <div class="foot_bg">
        <div class="container">
            <div class="foot_links">
                <ul class="first">
                    <h5>DC COMICS</h5>
                    <li v-for="(element, index) in Books" :key="index">{{element}}</li>
                </ul>
                <ul class="third">
                    <h5>DC</h5>
                    <li v-for="(element, index) in House" :key="index">{{ element }}</li>
                </ul>
                <ul class="fourth">
                    <h5>SITES</h5>
                    <li v-for="(element, index) in Web" :key="index">{{ element }}</li>
                </ul>
                <ul class="second">
                    <h5>SHOP</h5>
                    <li v-for="(element, index) in Buy" :key="index">{{ element }}</li>
                </ul>
            </div>
            
                <img class="foot_logo" src="../assets/dc-logo-bg.png" alt="logo dc">
            
        </div>
    </div>

</template>

<script>
    export default {
        name: 'TheFooterTop',
        props: {
            Books: Array,
            Buy: Array,
            House: Array,
            Web: Array
        }
    }
</script>

<style scoped lang="scss">
@use '../style/partials/variables' as *;
@use '../style/partials/mixins.scss';
    .foot_bg {
        height: 300px;
        background-image: url('../assets/footer-bg.jpg');
        display: flex;
    }

    .container {
        height: 100%;
        @include mixins.flex-center;
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

    h5 {
        color: $text-secondary;

    }

    li {
        color: $color-text;
        font-size: 10px;
        padding-top: .3rem;
        li:hover {
            color: $text-secondary;
        }
    }

    .foot_logo {
        width: 40%;
        height: 100%;
        object-fit: cover;
    }


</style>