<script>
export default {
    data() {
        return {
            linkList: [
                {
                    text: 'characters',
                    link: '#',
                },
                {
                    text: 'comics',
                    link: '#',
                },
                {
                    text: 'movies',
                    link: '#',
                },
                {
                    text: 'tv',
                    link: '#',
                },
                {
                    text: 'games',
                    link: '#',
                },
                {
                    text: 'collectibles',
                    link: '#',
                },
                {
                    text: 'videos',
                    link: '#',
                },
                {
                    text: 'fans',
                    link: '#',
                },
                {
                    text: 'news',
                    link: '#',
                },
                {
                    text: 'shop',
                    link: '#',
                },
            ]
        }
    }
}
</script>

<template>

    <header class="header">
        <div class="container">
            <div class="row">

                <a class="logo-wrapper" href="#">
                    <img src="/images/dc-logo.png" alt="">
                </a>


                <nav class="nav-bar">
                    <ul class="nav__list">
                        <li 
                        class="nav__item"
                        v-for="link in linkList"
                        >
                            <a href="#">
                                {{ link.text }}
                            </a>
                        </li>
                    </ul>
                </nav>

            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
.row {
    justify-content: space-between;
    align-items: center;

    .nav-bar {
        height: 100%;
    }
}

.logo-wrapper {
    display: block;
    padding: 10px 0;
    width: 75px;
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
        padding: 50px 15px;

        position: relative;

        &:hover {
            color: $main-blue;
        }

        &:hover::after {
            content: '';
            display: block;
            width: 50%;
            padding: 2px;
            background-color: $main-blue;

            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
    }

    .nav__item:last-child {
        margin-right: -15px;

        &:hover::after{
           transform: translateX(-50%);

        }
    }


}

</style>
