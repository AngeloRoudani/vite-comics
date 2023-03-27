<template>
    <header>
        <div class="container">
            <div class="image_logo">
                <img src="../assets/dc-logo.png" alt="logo dc">
            </div>
            <div class="link_list">
                <ul>
                    <li v-for="element in links"><a href="#">{{element}}</a><div class="border"></div></li>
                    
                </ul>
            </div>
        </div>
    </header>

</template>

<script>
    export default {
        name: "TheHeader",
            data() {
                return {
                    links: [ 'characters', 'comics', 'movies', 'tv', 'games', 'collectibles', 'videos', 'fans', 'news', 'shops' ],
                };
            },
        };
</script>




<style scoped lang="scss">

@use '../style/partials/mixins.scss';
@use '../style/partials/variables' as *;

header {
    background-color: $text-secondary;
}

.container {
    height: 80px;
    @include mixins.flex-center;
}

.image_logo img {
    height: 60px;
}

.link_list {
    height: 100%;
    @include mixins.flex-center;
    margin: 0;
    width: auto;
    ul {
        height: 100%;
        list-style: none;
        text-transform: uppercase;
        font-size: 12px;
        font-weight: bold;
        
        li {
            height: 90%;
            padding: 0 1rem ;
            display: inline-block;

            .border {
                width: 100%;
                height: 4px;
                background-color: $color-primary;
                display: none;
                margin-top: 31px;
            }

            a {
                text-decoration: none;
                color: black;
                padding-top: 30px;
                display: inline-block;
            }
            a:hover {
                color: $color-primary;
            } 
        }
        li:hover .border {
            display: block;
        }
        
    }
}



</style>
