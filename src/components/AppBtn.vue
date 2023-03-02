<script>
export default {
    props: {
        text: {
            type: String,
            required: true,
        }
    }

}


</script>


<template>

    <button class="btn">
        {{ text }}
    </button>

</template>


<style lang="scss">
@use '../style/partials/variables' as *;

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


</style>