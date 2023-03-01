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

    <header class="header">
        <div class="container">
            <div class="row">
                <div class="col">
                    <div class="logo-wrapper">
                        <img src="/images/dc-logo.png" alt="">
                    </div>
                </div>
                <div class="col">
                    <nav class="nav-bar">
                        <ul class="nav__list">
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">link</a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
.row {
    justify-content: space-between;
    align-items: center;
}

.nav__list {
    display: flex;

    .nav__item a {
        padding: 0 10px;
    }

    &::after {
        content: '';
        display: block;
        width: 10px;
        padding: 10px;
        background-color: $main-blue;
    }
}

</style>
