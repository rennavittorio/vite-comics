<script>
import AppCard from './AppCard.vue'

export default {
    components: {
        AppCard,
    },

    data() {
        return {
            example: 'exmaple',
            cardList: [
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://picsum.photos/200/300",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }

            ]
        }
    }
}
</script>

<template>

    <main class="main">
        <div class="container">
            
            <div class="jumbotron">
                jumbo...
            </div>

            <div class="cards__reel">

                <AppCard
                v-for="(card, i) in cardList" :key="i" :imageSrc="card.thumb" :text="card.series"
                class="card"
                />

            </div>


        </div>
    </main>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.main {
    background-color: $main-dark;
    color: $main-light;
    padding: 40px 0;

    position: relative;
    z-index: 999;
}

.cards__reel {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 20px;
    padding: 20px;

    .card:hover {
        color: $main-blue;
        box-shadow: 10px 5px 5px $main-blue;
    }
}



</style>
