<script>
    import AppCard from './AppCard.vue';

    export default {
        components:{
            AppCard,
        },
    }
</script>

<template>
<main class="page-content">
        <!-- sezione con gli articoli in vendita -->
        <section class="container">
            <div class="row">
                <div class="col-4">
                    <AppCard/>                    
                </div>               
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
    .page-content {
        padding: 60px 0;
    
        .col-4 {
            padding:20px 12px;
        }
    }
</style>