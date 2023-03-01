<script>
export default {
    data() {
        return {
            linkList: [
                { menu: 'dc comics', text: 'characters', link: '#', },
                { menu: 'dc comics', text: 'comics', link: '#', },
                { menu: 'dc comics', text: 'movies', link: '#', },
                { menu: 'dc comics', text: 'tv', link: '#', },
                { menu: 'dc comics', text: 'games', link: '#', },
                { menu: 'dc comics', text: 'videos', link: '#', },
                { menu: 'dc comics', text: 'news', link: '#', },

                { menu: 'shop', text: 'shop dc', link: '#', },
                { menu: 'shop', text: 'shop dc collectibles', link: '#', },

                { menu: 'dc', text: 'terms of use', link: '#', },
                { menu: 'dc', text: 'privacy policiy (new)', link: '#', },
                { menu: 'dc', text: 'ad choice', link: '#', },
                { menu: 'dc', text: 'advertising', link: '#', },
                { menu: 'dc', text: 'jobs', link: '#', },
                { menu: 'dc', text: 'subscriptions', link: '#', },
                { menu: 'dc', text: 'talent workshops', link: '#', },
                { menu: 'dc', text: 'CPSC certificates', link: '#', },
                { menu: 'dc', text: 'ratings', link: '#', },
                { menu: 'dc', text: 'shop help', link: '#', },
                { menu: 'dc', text: 'contact us', link: '#', },

                { menu: 'sites', text: 'dc', link: '#', },
                { menu: 'sites', text: 'mad magazine', link: '#', },
                { menu: 'sites', text: 'dc kids', link: '#', },
                { menu: 'sites', text: 'dc universe', link: '#', },
                { menu: 'sites', text: 'dc power visa', link: '#', },
            ]
        }
    },

    methods: {

    },

    computed: {
        getSubMenuDcComics(){
            return this.linkList.filter(obj => {
                return obj.menu === 'dc comics'
            });
        },

        getSubMenuShop(){
            return this.linkList.filter(obj => {
                return obj.menu === 'shop'
            });
        },

        getSubMenuDc(){
            return this.linkList.filter(obj => {
                return obj.menu === 'dc'
            });
        },

        getSubMenuSites(){
            return this.linkList.filter(obj => {
                return obj.menu === 'sites'
            });
        },
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
                            <span class="menu__title">
                                {{ getSubMenuDcComics[0].menu }}
                            </span> 
                            <li 
                            class="footer__menu__item"
                            v-for="link in getSubMenuDcComics"
                            >
                                <a href="">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
    
                        <ul class="footer__menu">
                            <span class="menu__title">
                                {{ getSubMenuShop[0].menu }}
                            </span> 
                            <li 
                            class="footer__menu__item"
                            v-for="link in getSubMenuShop"
                            >
                                <a href="">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
    
                    </div>
    
                    <div class="col">
                        <ul class="footer__menu">
                            <span class="menu__title">
                                {{ getSubMenuDc[0].menu }}
                            </span> 
                            <li 
                            class="footer__menu__item"
                            v-for="link in getSubMenuDc"
                            >
                                <a href="">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
    
                    <div class="col">
                        <ul class="footer__menu">
                            <span class="menu__title">
                                {{ getSubMenuSites[0].menu }}
                            </span> 
                            <li 
                            class="footer__menu__item"
                            v-for="link in getSubMenuSites"
                            >
                                <a href="">
                                    {{ link.text }}
                                </a>
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

    .footer__logo-wrapper{
        position: absolute;
        width: 100%;
        bottom: 0;
        left: 0;
        transform: translate(50%, -25%);
        z-index: 0;

    }




    .col {
        padding-right: 100px;
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

        position: relative;
        z-index: 999;

        span {
            font-size: 2rem;
            font-weight: 700;
            text-transform: uppercase;
        }

        .footer__menu__item {
            font-size: 1rem;
            font-weight: 300;
            text-transform: capitalize;
            padding: 10px 0;

            &:hover {
                color: $main-blue;
            }
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
