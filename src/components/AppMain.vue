<script>
    export default {

    }
</script>

<template>
<main class="page-content">
        <!-- sezione con gli articoli in vendita -->
        <section class="container">
            <div class="row">
                <div class="col-4">
                    <!-- immagine e testo dell'articolo 1 in vendita -->
                    <div class="card">
                        <div class="card-head">
                            <!-- cuoricino preferiti -->
                            <div class="heart">
                                <a href="">&hearts;</a>
                            </div>
                                <!-- immagine -->
                                <img src="../assets/img/1.webp" alt="">
                            <div>
                                <!-- badge -->
                                <div class="badge discount">-50%</div>
                                <div class="badge sostenibility">Sostenibilità</div>
                            </div>
                            <div class="overlay">
                                <!-- immagine overlay -->
                                <img src="../assets/img/1b.webp" alt="">
                            </div>                        
                        </div>
                        <div class="card-foot">
                            <!-- testo con descrizione e prezzo -->
                            <h5 class="brand">Levi's</h5>
                            <h3 class="description">RELAXED FIT TEE UNISEX</h3>                         
                            <span class="price">14,99€</span>
                            <span class="first-price">29,99€</span>                        
                        </div>
                    </div>
                </div>

                <div class="col-4">
                    <!-- immagine e testo dell'articolo 2 in vendita -->
                    <div class="card">
                        <div class="card-head">
                            <div class="heart">
                                <a href="">&hearts;</a>
                            </div>
                                <img src="../assets/img/2.webp" alt="">
                            <div>
                                <div class="badge discount">-30%</div> 
                            </div>
                            <div class="overlay">
                                <img src="../assets/img/2b.webp" alt="">
                            </div>  
                        </div>
                        <div class="card-foot">
                            <h5 class="brand">Guess</h5>
                            <h3 class="description">ROSES TEE</h3>                        
                            <span class="price">20,99€</span>
                            <span class="first-price">29,99€</span>                        
                        </div>
                    </div>
                </div>

                <div class="col-4">
                    <!-- immagine e testo dell'articolo 3 in vendita -->
                    <div class="card">
                        <div class="card-head">
                            <div class="heart">
                                <a href="">&hearts;</a>
                            </div>
                                <img src="../assets/img/3.webp" alt="">
                            <div>
                                <div class="badge discount">-30%</div>
                            </div>
                            <div class="overlay">
                                <img src="../assets/img/3b.webp" alt="">
                            </div>  
                        </div>
                        <div class="card-foot">
                            <h5 class="brand">Come Zucchero Filato</h5>
                            <h3 class="description">VOGLIA DI COLORI PASTELLO</h3>                            
                            <span class="price">129,99€</span>
                            <span class="first-price">184,99€</span>                            
                        </div>
                    </div>
                </div>

                <div class="col-4">
                    <!-- immagine e testo dell'articolo 4 in vendita -->
                    <div class="card">
                        <div class="card-head">
                            <div class="heart">
                                <a href="">&hearts;</a>
                            </div>
                                <img src="../assets/img/4.webp" alt="">
                            <div>
                                <div class="badge discount">-50%</div>
                                <div class="badge sostenibility">Sostenibilità</div>
                            </div>
                            <div class="overlay">
                                <img src="../assets/img/4b.webp" alt="">
                            </div>  
                        </div>
                        <div class="card-foot">
                            <h5 class="brand">Levi's</h5>
                            <h3 class="description">TEE UNISEX</h3>                          
                            <span class="price">19,99€</span>
                            <span class="first-price">29,99€</span>                            
                        </div>
                    </div>
                </div>

                <div class="col-4">
                    <!-- immagine e testo dell'articolo 5 in vendita -->
                    <div class="card">                    
                        <div class="card-head">
                            <div class="heart">
                                <a href="">&hearts;</a>
                            </div>
                                <img src="../assets/img/5.webp" alt="">
                            <div class="overlay">
                                <img src="../assets/img/5b.webp" alt="">
                            </div>  
                        </div>
                        <div class="card-foot">
                            <h5 class="brand">Maya Deluxe</h5>
                            <h3 class="description">STRIPE BODICE</h3>                          
                            <span class="price">99,99€</span>                        
                        </div>
                    </div>
                </div>

                <div class="col-4">
                    <!-- immagine e testo dell'articolo 6 in vendita -->
                    <div class="card">
                        <div class="card-head">
                            <div class="heart">
                                <a href="">&hearts;</a>
                            </div>
                                <img src="../assets/img/6.webp" alt="">
                            <div>
                                <div class="badge sostenibility">Sostenibilità</div>
                            </div>
                            <div class="overlay">
                                <img src="../assets/img/6b.webp" alt="">
                            </div>  
                        </div>
                        <div class="card-foot">
                            <h5 class="brand">Esprit</h5>
                            <h3 class="description">MAGLIONE - BLACK</h3>
                            <span class="price">29,99€</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;
    .page-content {
        padding: 60px 0;
    
        .col-4 {
            padding:20px 12px;
        }
    }
    .card-head{
        position: relative;
        
        &:hover .overlay{
        opacity: 1;
        transition: opacity 400ms ease-in-out;
        }
    }

    .brand{
        font-weight: 400;
        font-size: $font-size;
    }

    .description{
        font-size: 14px;
        line-height: 12px;
    }
    .price, .first-price{
        font-size: $font_size;
    }

    .price{
        font-weight: 700;
        color: red;
    }
    .first-price{
        text-decoration: line-through;
        padding-left: 10px;
    }
    .badge{
        font-weight: 700;
        font-size:14px ;
        position: absolute;
        color: white;
        bottom: 30px; 
        z-index: 10;
        
        &:nth-child(2){
            left:38px;
        }
    }
    .discount{
        background-color: red;
    }
    .sostenibility{
        background-color: green;
    }
  
    .heart{  
        position: absolute;
        background-color: white;
        text-align: center;
        font-size: 22px;
        width: 36px;
        height: 36px;
        top: 4px;
        right: 0;
        z-index:10;

        &:hover{
        color: red;
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
</style>