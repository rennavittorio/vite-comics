<script>
export default {
    data() {
        return {
            example: 'exmaple'
        }
    }
}
</script>

<template>

    <footer class="footer">
        <div class="footer__links">

            <div class="container">

                <div class="footer__logo-wrapper">
                    <img src="/images/dc-logo-bg.png" alt="">
                </div>
                
                <div class="row">
                    <div class="col">
    
                        <ul class="footer__menu">
                            <span>Dc comics</span> 
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                        </ul>
    
                        <ul class="footer__menu">
                            <span>Dc comics</span> 
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                        </ul>
    
                    </div>
    
                    <div class="col">
                                            <ul class="footer__menu">
                            <span>Dc comics</span> 
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                        </ul>
                    </div>
    
                    <div class="col">
                                            <ul class="footer__menu">
                            <span>Dc comics</span> 
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                            <li class="footer__menu__item">
                                <a href="">link</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            

        </div>

        <div class="footer__stay-in-touch">

            <div class="container">

                <div class="row">
                    <div class="col">
                        <button class="btn sign-up">
                            Sign-up now
                        </button>
                    </div>
                    <div class="col follow-us">
                        <a href="">
                            <h1>
                                Follow us
                            </h1>
                        </a>
                        <div class="social-logo-wrapper">
                            <a href="#"><img src="/images/footer-facebook.png" alt=""></a> 
                        </div>
                        <div class="social-logo-wrapper">
                            <a href="#"><img src="/images/footer-twitter.png" alt=""></a> 
                        </div>
                        <div class="social-logo-wrapper">
                            <a href="#"><img src="/images/footer-youtube.png" alt=""></a> 
                        </div>
                        <div class="social-logo-wrapper">
                            <a href="#"><img src="/images/footer-pinterest.png" alt=""></a> 
                        </div>
                        <div class="social-logo-wrapper">
                            <a href="#"><img src="/images/footer-periscope.png" alt=""></a> 
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </footer>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.footer {
    color: $main-light;
    position: relative;

    .container {


    }

    .footer__logo-wrapper{
        position: absolute;
        width: 100%;
        transform: translate(35%, -15%);
        z-index: 0;

    }




    .col {
        padding-right: 50px;
    }

    .footer__links {
        background-image: url('/images/footer-bg.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        padding: 50px 0;

    }

    .footer__menu {

        margin-bottom: 20px;

        span {
            font-size: 2rem;
            font-weight: 700;
        }

        .footer__menu__item {
            font-size: 1rem;
            padding: 10px 0;
        }

    }
    
    .footer__stay-in-touch {
        background-color: $main-dark;
        padding: 50px 0;
        position: relative;
        z-index: 999;

        .row {
            justify-content: space-between;
            align-items: center;

            .follow-us {
                display: flex;
                align-items: center;

                * {
                    padding-left: 10px;
                    display: block;
                    flex-shrink: 0;
                }

                h1 {
                    color: $main-blue;
                    text-transform: uppercase;
                    font-size: 1.5rem;
                }

                .social-logo-wrapper:hover {
                    transform: scale(1.2);
                }

            }
        }


        .btn {
            padding: 10px;
            text-transform: uppercase;
            background-color: transparent;
            color: $main-light;
            border: 2px solid $main-blue;

            &:hover {
                background-color: $main-blue;
                color: $main-dark;
                cursor: pointer;
            }
        }

    }


}


</style>
