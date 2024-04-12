<script>
import AppCard from './AppCard.vue';
import {store} from '../store'

export default {

    components: {
        AppCard,
    },
    data() {
        return {
            store
        }
    },
}
</script>

<template>
    <main class="page-content">
        <!-- sezione con gli articoli in vendita -->
        <section class="container">
            <div class="row">
                <div v-for="product in store.db" :key="product.id" class="col-4">
                    <AppCard :card="product" :reMapCard="store.mappedDb[(product.id) - 1]" />
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
.page-content {
    padding: 60px 0;

    .col-4 {
        padding: 20px 12px;
    }
}
</style>