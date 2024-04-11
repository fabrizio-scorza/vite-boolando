<script>
    import AppCard from './AppCard.vue';
    import items from '../assets/db.json'

    export default {
        components:{
            AppCard,
        },
        data(){
            return{
                items: items.products,   
            }
        }
    }
</script>

<template>
<main class="page-content">
        <!-- sezione con gli articoli in vendita -->
        <section class="container">
            <div class="row">
                <div v-for="product in items" class="col-4">
                    <AppCard :card="product" :key="product.id"/>                    
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