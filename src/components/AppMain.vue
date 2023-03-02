<script>
import AppCard from './AppCard.vue';
import AppBtn from './AppBtn.vue';

export default {
    components: {
        AppCard,
        AppBtn,
    },

    data() {
        return {
            example: 'exmaple',
            cardList: [
                {
                    "thumb": "images/acquaman-cover1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "images/batman-cover1.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "images/acquaman-cover1.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "images/batman-cover2.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "images/batman-cover1.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "images/batman-cover2.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "images/superman-cover1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "images/superman-cover1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "images/joker-cover1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "images/joker-cover1.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "images/quinn-cover1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "images/catwoman-cover1.jpg",
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

        <div class="jumbotron">
            <div class="container">

                <AppBtn text="Current seires" class="btn-large" />

            </div>
        </div>

        <div class="container">
            
            <div class="cards__reel">

                <AppCard
                v-for="(card, i) in cardList" :key="i" :imageSrc="card.thumb" :text="card.series"
                class="card"
                />

            </div>

        </div>

        <AppBtn text="Load more" class="btn-large" />

    </main>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.main {
    background-color: $main-dark;
    color: $main-light;
    padding-bottom: 40px;

    position: relative;
    z-index: 999;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.jumbotron {
    width: 100%;
    height: 300px;
    background-image: url(/images/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: top;

    .container {
        position: relative;
        height: 100%;
    
        .btn-large {
            position: absolute;
            padding: 10px;
            bottom: 0;
            left: 0;
            transform: translateY(50%);
        }

    }

}

.cards__reel {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 20px;
    padding: 75px 0;

    .card:hover {
        color: $main-blue;
        box-shadow: 10px 5px 5px $main-blue;
    }
}

.btn-large {
    width: fit-content;
    padding: 10px 60px;
    background-color: $main-blue;

    &:hover {
        background-color: $main-light;
        color: $main-blue;
        // border: 1px solid $main-blue;
        box-shadow: 10px 5px 0px $main-blue;

    }
}



</style>
