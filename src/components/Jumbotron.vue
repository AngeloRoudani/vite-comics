<template>
    <div class="jumbo">
        <div class="label">current series</div>
    </div>

</template>
<script>
    export default {
        name: 'Jumbotron'
    }
</script>
<style scoped lang="scss">
    @use '../style/partials/variables' as *;
    .jumbo {
        height: 350px;
        background-image: url('../assets/jumbotron.jpg');
        position: relative;
    }

    .label {
        width: 200px;
        height: 30px;
        background-color: $color-primary;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 18px;
        text-align: center;
        position: absolute;
        bottom: -15px;
        left: 350px;
        color: $text-secondary;
        padding-top: 5px;
    }

</style>