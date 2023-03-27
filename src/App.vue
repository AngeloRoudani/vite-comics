
<template>

        <TheHeader/>
    <main>
        <TheMain/>
    </main>
    <footer>
        <TheFooterTop/>
        <TheFooterBottom/>
    </footer>

</template>

<script>

    import TheHeader from './components/TheHeader.vue';
    import TheMain from './components/TheMain.vue'
    import TheFooterTop from './components/TheFooterTop.vue';
    import TheFooterBottom from './components/TheFooterBottom.vue';

    export default {
        components : {
            TheHeader,
            TheFooterTop,
            TheMain,
            TheFooterBottom
        }
    }
</script>

<style scoped lang="scss">
    @use './style/general.scss';
</style>
