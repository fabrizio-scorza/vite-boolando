<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';
    import AppFooter from './components/AppFooter.vue';

    export default {
        components: {
            AppHeader,
            AppMain,
            AppFooter,
        }
    }
</script>

<template>
    <AppHeader/>
    <AppMain/>
    <AppFooter/>
</template>

<style lang="scss">
    @use './style/general';

    body{
        font-family: 'Open Sans', sans-serif;
    }
</style>
