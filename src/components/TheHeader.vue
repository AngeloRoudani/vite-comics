<template>
    <header>
        <div class="container">
            <div class="image_logo">
                <img src="../assets/dc-logo.png" alt="logo dc">
            </div>
            <div class="link_list">
                <ul>
                    <li v-for="element in links"><a href="#">{{element}}</a></li>
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

header {
    background-color: white;
}

.container {
    width: 1170px;
    height: 80px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.image_logo img {
    height: 60px;
}

.link_list {
    height: 100%;
    display: flex;
    align-items: center;
    ul {
        height: 100%;
        list-style: none;
        text-transform: uppercase;
        font-size: 12px;
        font-weight: bold;
        
        li {
            height: 100%;
            padding: 0 1rem ;
            display: inline-block;

            li:hover {
                border-bottom: solid 3px #0282f9;
            }

            a {
                text-decoration: none;
                color: black;
                vertical-align: center;
                padding-top: 30px;
                display: inline-block;
            }
            a:hover {
            color: #0282f9;
            }
        
            
        }
        
    }
}



</style>
