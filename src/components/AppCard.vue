<script>
    export default {
        props: ['card','badges','reMapCard'],
        
        data(){
            return{

            }
        },
        methods:{            
            calcPrice(item) {
                const newPrice = item.price -(item.price*item.discount/100);
                return newPrice.toFixed(2)               
            }
        }
    }
</script>

<template>
    <div class="card">
        <div class="card-head">
            <!-- cuoricino preferiti -->
            <div class="heart">
                <a v-if="card.isInFavorites" href="">
                    <i class="fa-solid fa-heart"></i>                    
                </a>
                <a v-else>
                    <i class="fa-regular fa-heart"></i>
                </a>
            </div>
            <!-- immagine -->
            <img :src="'/img/'+card.frontImage" alt="">
            <div>
                <div v-for="badge in badges" class="badge" :class="badge.type">
                    <!-- badge -->
                        {{ badge.value }}
                    <!-- <div class="badge sostenibility">Sostenibilità</div> -->
                </div>
            </div>
            <div class="overlay">
                <!-- immagine overlay -->
                <img :src="'/img/'+card.backImage" alt="">
            </div>                        
        </div>
        <div class="card-foot">
            <!-- testo con descrizione e prezzo -->
            <h5 class="brand">
                {{ card.brand }}
            </h5>
            <h3 class="description">
                {{ card.name.toUpperCase() }}
            </h3>
            <div v-if="reMapCard.isDiscounted">
                <span class="price">
                    {{ calcPrice(reMapCard) }}
                </span>                     
                <span class="first-price">
                    {{ card.price }}
                </span>
            </div>
            <div v-else>
                <span class="price">
                    {{ card.price }}
                </span>
            </div>                           
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;
    
    .card{
        cursor: pointer;
        
        &:hover .overlay{
        opacity: 1;
        transition: opacity 400ms ease-in-out;
        }
    }

    .overlay{
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        opacity: 0;
    }
    
    .card-head{
        position: relative;
    }

    .badge{
        font-weight: 700;
        font-size: $font-size;        
        color: white;
        position :absolute;
        bottom: 30px;
        z-index: 2;

        &:first-child:not(:only-child){
            left:38px;
        }
    }
    .discount{
        background-color: red;
    }
    .tag{
        background-color: green;
    }
  
    .heart{  
        position: absolute;
        background-color: white;
        text-align: center;
        font-size: 18px;
        line-height: 36px;;
        width: 36px;
        aspect-ratio: 1;
        top: 4px;
        right: 4px;
        z-index:2;

        &:hover{
        color: red;
        }
    } 

    .brand{
        font-weight: 400;
        font-size: $font-size;
    }

    .description{
        font-size: $font-size;
        line-height: 12px;
    }
    .price, .first-price{
        font-size: $font_size;
        &::after{
            content: '€';
        }
    }

    .price{
        font-weight: 700;
        color: red;
    }
    .first-price{
        text-decoration: line-through;
        padding-left: 10px;
    }
    
</style>SS