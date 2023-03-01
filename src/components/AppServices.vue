<script>
export default {
    data() {
        return {
            linkList: [
                { icon: '/images/buy-comics-digital-comics.png', text: 'digital comics', },
                { icon: '/images/buy-comics-merchandise.png', text: 'dc merchandise', },
                { icon: '/images/buy-comics-subscriptions.png', text: 'subscription', },
                { icon: '/images/buy-comics-shop-locator.png', text: 'comic shop locator', },
                { icon: '/images/buy-dc-power-visa.svg', text: 'dc power visa', },
            ]
        }
    }
}
</script>

<template>

    <section class="services">
        <div class="container">

            <div class="row">

                <ul class="services__list">
                    <li 
                    class="service__item"
                    v-for="service in linkList"
                    >
                        <div class="img-wrapper">
                            <img :src="service.icon" alt="">
                        </div>
                        <div class="service__name">
                            {{ service.text }}
                        </div>
                    </li>
                </ul>

            </div>

        </div>
    </section>

</template>

<style lang="scss">
@use '../style/partials/variables' as *;

.services {
    background-color: $main-blue;
    color: $main-light;

    .row {
        justify-content: center;
        align-items: center;


        .services__list {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .service__item {
                display: flex;
                align-items: center;

                padding: 40px 25px;


                .img-wrapper {
                    max-width: 35px;
                    height: 35px;
                    object-fit: contain;
                    object-position: center;
                    margin-right: 10px;

                    img {
                        width: 100%;
                        height: 100%;
                    }
                }

                .service__name {
                    text-transform: uppercase;
                }
            }
        }
    }


}

</style>