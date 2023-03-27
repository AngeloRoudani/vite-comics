
<template>

        <TheHeader/>
    <main>
        <TheMain/>
    </main>
    <footer>
        <TheFooterTop/>
    </footer>

</template>

<script>

    import TheHeader from './components/TheHeader.vue';
    import TheMain from './components/TheMain.vue'
    import TheFooterTop from './components/TheFooterTop.vue';

    export default {
        components : {
            TheHeader,
            TheFooterTop,
            TheMain
        }
    }
</script>

<style scoped lang="scss">

</style>
