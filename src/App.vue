<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';

    export default {
        components: {
            AppHeader,
            AppMain,
        }
    }
</script>

<template>
    <AppHeader/>
    <AppMain/>
</template>

<style lang="scss">
    @use './style/general';

    body{
        font-family: 'Open Sans', sans-serif;
    }
</style>
