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

    <main class="main">
        <div class="container">
            content here...
        </div>
    </main>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;

.main {
    background-color: $main-dark;
    color: $main-light;
    padding: 40px 0;
}

</style>
