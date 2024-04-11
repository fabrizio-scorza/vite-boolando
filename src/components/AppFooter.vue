<script>
    export default {

    }
</script>

<template>
    <footer class="page-footer">
        <div class="container">
            <div class="row">
                <div class="info">
                    <h4>Boolando s.r.l</h4>
                    <ul>
                        <li>
                            <a href="">Informazioni legali</a>
                        </li>
                        <li>
                            <a href="">Informativa sulla privacy</a>
                        </li>
                        <li>
                            <a href="">Diritto di recesso</a>
                        </li>
                    </ul>
                </div>
                <div class="social">
                    <h4>Trovaci anche su</h4>
                    <ul>
                        <li>
                            <a href="#">
                                <img src="/img/twitter_alt.svg" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="/img/facebook_alt.svg" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="/img/instagram-alt.svg" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="/img/pinterest.svg" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="/img/youtube_alt.svg" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
    @use '../style/partials/variables' as *;

    .page-footer{        
        background-color:#1A1A1A ;
        font-weight: 500;
        font-size: $font-size;
        color: white;
        padding: 20px 0;

        .row{
            justify-content: space-between;
            align-items:flex-start;
        }
    }
   
    .info{ 
        h4{
            font-weight:700;
            font-size:22px;
        }
        ul{
            display: flex;
            flex-wrap: wrap;
            font-weight: 300;
            font-style: italic;
            font-size: 12px;
        }
        a{
            padding-right:12px ;
        }
    }
    .social{
        ul, a{
            display: flex;
            flex-wrap: wrap;
        }
        h4{
            font-size: $font-size;
            margin-bottom: 8px;
        }
        a{
            margin-right: 8px;
            background-color: white;
            border-radius: 5px;
        }
        img{
            width: 18px;
            filter:invert(6%) sepia(5%) saturate(147%) hue-rotate(315deg) brightness(98%) contrast(91%);
        }
    }
</style>