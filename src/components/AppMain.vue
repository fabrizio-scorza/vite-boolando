<script>
import AppCard from './AppCard.vue';
import ModalCard from './ModalCard.vue';
import {store} from '../store'

export default {

    components: {
        AppCard,
        ModalCard,
    },
    data() {
        return {
            store,
            visibility: false,
            index:0,
        }
    },
    methods:{
        openModal(index){
            this.visibility = true;
            this.index = index;
        },
        closeModal(){
            this.visibility = false;
        }
    }
}
</script>

<template>
    <main class="page-content">
        <!-- sezione con gli articoli in vendita -->
        <section class="container">
            <div class="row">
                <div v-for="(product, i) in store.db" :key="product.id" class="col-4">
                    <AppCard :card="product" :reMapCard="store.mappedDb[(product.id) - 1]" @showProduct="openModal(i)"/>
                </div>
                <ModalCard v-if="visibility" :card="store.db[index]" @closeProduct="closeModal()"/> 
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