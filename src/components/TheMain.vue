<template>
    <section class="top">
        <div class="container">
            <h1 class="title">Content goes here</h1>
        </div>
        
    </section>
    <section class="bottom">
        <div class="bottom_bg">

        </div>
    </section>
</template>

<script>
    export default {
        name: 'TheMain'
    }
</script>

<style scoped lang="scss">

@use '../style/partials/variables' as *;
    .top {
        height: 100px;
        background-color: #1c1c1c;
        h1 {
            width: 1170px;
            color: $text-secondary;
        }
    }
    .container {
        width: 1170px;
        margin: auto;
    }

    .bottom {
        height: 120px;
        background-color: $color-primary;
    }
</style>