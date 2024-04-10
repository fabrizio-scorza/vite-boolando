<script>
    export default {

    }
</script>

<template>
    <header class="page-header">
        <nav class="container">
            <div class="flex">
                <!-- menù -->
                <ul class="flex">                    
                    <li>
                        <a href="#">Donna</a>
                    </li>
                    <li>
                        <a href="#">Uomo</a>
                    </li>
                    <li>
                        <a href="#">Bambino</a>
                    </li>
                </ul>                 
                <div class="logo">
                    <!-- logo -->
                    <img src="../assets/img/boolean-logo.png" alt="">
                </div>
                <ul class="action flex">
                    <!-- icone link -->
                    <li>
                        <a href="">
                            <img src="../assets/img/user-icon.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <img src="../assets/img/love-icon.png" alt="">
                        </a>
                    </li> 
                    <li>
                        <a href="">
                            <img src="../assets/img/bag-icon.png" alt="">
                        </a>
                    </li>                   
                </ul>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
    .page-header{
        background-color:#FF6900;
        font-weight: 600;
        font-size: 14px;
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