<script>
export default {
    props: {
        imageSrc: {
            type: String,
            required: true,
        },
        text: {
            type: String,
            required: true,
        }
    }

}


</script>

<template>

    <div class="card">
        <div class="card__img">
            <img :src="imageSrc" alt="">
        </div>
        <div class="card__text">
            {{ text }}
        </div>
    </div>

</template>


<style lang="scss">
.card {
    max-width: 100%;


    .card__img {

        margin-bottom: 20px;
    
        img {
            max-width: 100%;
            aspect-ratio: 3 / 4;
            object-fit: cover;
            object-position: center;
    
        }
    }

    .card__text {
        text-transform: uppercase;
        font-size: 0.75rem;
    }
}

</style>