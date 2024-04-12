<script>
import axios from 'axios'
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import {store} from './store'

export default {
    components: {
        AppHeader,
        AppMain,
        AppFooter,
    },
    data() {
        return {
            store,
            id: 0,
            price: 0,
            isDiscounted: false,
            discount: 0,
        }
    },
    methods: {
        extractedData(items) {
            console.log(items);
            items.forEach(item => {
                item.badges.forEach(badge => {
                    if (badge.type === 'discount') {
                        this.isDiscounted = true;
                        this.discount = parseInt(badge.value.slice(1, 3))
                    }
                })

                this.store.mappedDb.push({
                    id: item.id,
                    price: item.price,
                    isDiscounted: this.isDiscounted,
                    discount: this.discount
                })

                this.isDiscounted = false;
                this.discount = 0
            })
        }
    },        
    mounted(){
        axios.get('http://localhost:3000/products').then((response)=>{
            const data = response.data
            this.store.db = data
            this.extractedData(this.store.db)
        })
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
S
body {
    font-family: 'Open Sans', sans-serif;
}
</style>
