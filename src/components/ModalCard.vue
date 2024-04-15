<script>
export default {
    props: ['card'],

    data() {
        return {
        }
    }  
}
</script>

<template>
    <div class="modal__card">
        <div class="card-header">
            <img :src="'/img/' + card.frontImage" alt="">
        </div>
        <div class="card-description">
            <h5 class="brand">
                {{ card.brand }}
            </h5>
            <h3 class="description-title">
                {{ card.name.toUpperCase() }}
            </h3>
            <p class="description">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam reiciendis reprehenderit commodi ea repellat. Facilis expedita quisquam doloribus veniam similique voluptatem iste, aut odio quam labore harum neque impedit dolore.
            </p>
        </div>
        <span class="btn" @click="$emit('closeProduct')">X</span>
    </div>
</template>

<style lang="scss" scoped>
    .modal__card{
        position:fixed;
        left: 50%;
        bottom:25%;
        transform: translateX(-50%);
        z-index: 3;
        display:flex;
        gap: 20px;
        width: 800px;
        height: 450px;
        background-color: white;
        border: 2px solid black;
        align-items: center;
    }
    .card-header{
        height: 100%;

        img{
            display: block;
            height: 100%;
            aspect-ratio: 16/9;
            object-fit: cover;
        }
       
    }
    .card-description > *{
        padding-bottom:15px;
    }

    .btn{
        align-self: flex-start;
        padding: 10px;
        color: red;
        font-size: 18px;
        font-weight: 900;
        cursor: pointer;
        }
</style>