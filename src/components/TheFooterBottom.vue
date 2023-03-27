<template>
    <div class="bottom">
        <div class="container">
            <button class="btn">sign-up now</button>
            <div class="icons">
                <span>FOLLOW US</span>
                <ul>
                    <li v-for="element in icons">
                        <a href="#">
                            <i class="fa-brands" :class="'fa-'+ element"></i>
                        </a></li>
                </ul>
            </div>
        </div>
    </div>

</template>

<script>

    export default {
        name: 'TheFooterBottom',
        data () {
            return {
            icons: ['facebook', 'twitter','youtube', 'pinterest', 'instagram'] 
            }
        }
    }
</script>

<style scoped lang="scss">

    .bottom {
        background-color: #303030;
    }
    .container {
        width: 1170px;
        margin: auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2rem 0;

    }

    .icons {
        width: 30%; 
        padding-left: 2rem;

    }
    span {
        color: #0282f9;
        font-weight: bold;
        padding-right: 1.5rem;
    }

    i {
        color: #959595;
        font-size: 1.5rem;
        padding-right: .5rem;
    }

    

    ul {
        list-style: none;
        display: inline-block;
        li {
            display: inline-block;
        }
    }

    .btn {
        padding: .5rem;
        border: solid 2px #0282f9;
        color: white;
        background-color: #303030;
        text-transform: uppercase;
        font-weight: bold;

    }
</style>
