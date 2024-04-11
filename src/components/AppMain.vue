<script>
    import AppCard from './AppCard.vue';
    import items from '../assets/db.json'

    export default {
        components:{
            AppCard,
        },
        data(){
            return{
                itemList: items.products,
                mappedCards:[],
                id: 0,
                price: 0,
                isDiscounted: false,
                discount: 0,   
            }
        },
        methods:{
            extractedData(items){
                items.forEach( item => {
                    item.badges.forEach( badge => {
                        if (badge.type === 'discount'){
                            this.isDiscounted = true;
                            this.discount = parseInt(badge.value.slice(1,3))
                        }                        
                    })

                    this.mappedCards.push({
                        id : item.id,
                        price : item.price,
                        isDiscounted : this.isDiscounted,
                        discount : this.discount
                    })
                    this.isDiscounted = false;
                    this.discount = 0
                })
            },
        }, 
        created () {
            this.extractedData(this.itemList)
            console.log(this.mappedCards[1].isDiscounted)
        }
    }
</script>

<template>
<main class="page-content">
        <!-- sezione con gli articoli in vendita -->
        <section class="container">
            <div class="row">
                <div v-for="(product) in itemList" class="col-4">
                    <AppCard :card="product" :badges="product.badges" :reMapCard="mappedCards[(product.id)-1]" :key="product.id"/>                    
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