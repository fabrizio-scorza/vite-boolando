<script>
    export default {
        data(){
            return{
                categories:['Donna', 'Uomo', 'Bambino'],
                icons: ['user-icon.png', 'love-icon.png', 'bag-icon.png']
                
            }
        }
    }
</script>

<template>
    <header class="page-header">
        <nav class="container">
            <div class="flex">
                <!-- menù -->
                <ul class="flex">                    
                    <li v-for="category in categories">
                        <a href="#">
                            {{category}}
                        </a>
                    </li>
                </ul>                 
                <div class="logo">
                    <!-- logo -->
                    <img src="../assets/img/boolean-logo.png" alt="">
                </div>
                <ul class="action flex">
                    <!-- icone link -->
                    <li v-for="icon in icons">
                        <a href="">
                            <img :src="'../assets/img/'+ icon" alt="">
                        </a>
                    </li>                 
                </ul>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;
    .page-header{
        background-color:#FF6900;
        font-weight: 600;
        font-size: $font-size;
        color:white;
        width: 100%;
        position: fixed;
        z-index: 100;
        padding: 12px 0;

        .flex{
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 8px;
        }
    }

    .logo img{
        height: 28px;
    }

    .action img{
        width: 20px;
    }
</style>