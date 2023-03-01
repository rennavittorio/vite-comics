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
                                <a href="#">Characters</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Comics</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Movies</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Tv</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Games</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Collectibles</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Videos</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Fans</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">News</a>
                            </li>
                            <li class="nav__item">
                                <a href="#">Shop</a>
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

.logo-wrapper {
    padding: 10px;
}

.nav__list {
    display: flex;


    .nav__item {

        display: flex;
        flex-direction: column;
        align-items: center;
        font-size: 1rem;
        font-weight: 700;
        text-transform: uppercase;
        line-height: 40px;
        padding: 0 10px;

        position: relative;

        &:hover {
            color: $main-blue;
        }

        &:hover::after {
            content: '';
            display: block;
            width: 10px;
            padding: 2px;
            background-color: $main-blue;

            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
    }


}

</style>
