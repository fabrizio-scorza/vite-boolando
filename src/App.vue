<script>
    import AppHeader from './components/AppHeader.vue';

    export default {
        components: {
            AppHeader,
        }
    }
</script>

<template>
    <AppHeader/>
</template>

<style lang="scss">
    @use './style/general';

    body{
        font-family: 'Open Sans', sans-serif;
    }
</style>
