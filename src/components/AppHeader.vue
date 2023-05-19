<link rel="stylesheet" href="../assets/styles/main.sass">
<template>
    <div class="header-wrapper">
        <div class="container">
            <div class="header__logo">
                <a href="#"><img src="../../public/img/dc-logo.png" alt="logo img"/></a>
            </div>
            <nav class="navbar">
                <ul class="nav-list">
                    <li class="nav-item"><a href="#">CHARACTERS</a></li>
                    <li class="nav-item active"><a href="#">COMICS</a></li>
                    <li class="nav-item"><a href="#">MOVIES</a></li>
                    <li class="nav-item"><a href="#">TV</a></li>
                    <li class="nav-item"><a href="#">GAMES</a></li>
                    <li class="nav-item"><a href="#">COLLECTIBLES</a></li>
                    <li class="nav-item"><a href="#">VIDEOS</a></li>
                    <li class="nav-item"><a href="#">FANS</a></li>
                    <li class="nav-item"><a href="#">NEWS</a></li>
                    <li class="nav-item"><a href="#">SHOP</a></li>
                </ul>
            </nav>
        </div>
    </div>
    <div class="jumbo-wrapper">
        <img src="../../public/img/jumbotron.jpg" alt=""/>
    </div>
</template>

<script>
export default {
    name: "AppHeader"
}
</script>

<style lang="sass" scoped>
@import "src/assets/styles/partials/variables"

.container
    padding-inline: 10px
    display: flex
    justify-content: space-between

    .header__logo
        padding: 20px

    .navbar
        $border-bottom-width: 7px
        $link-padding: 10px

        .nav-list
            list-style: none
            display: flex
            height: 100%

            .nav-item
                height: 100%
                display: flex
                place-items: center

                &:hover
                    color: $color-blue
                    border-bottom: $border-bottom-width solid $color-blue
                    margin-bottom: -$border-bottom-width

                    a
                        margin-bottom: -$border-bottom-width

                a
                    height: 100%
                    padding: $link-padding
                    display: flex
                    place-items: center
                    font-weight: bold

            .active
                color: $color-blue
                border-bottom: $border-bottom-width solid $color-blue
                margin-bottom: -$border-bottom-width

                a
                    margin-bottom: -$border-bottom-width

.jumbo-wrapper
    display: flex

    img
        object-fit: cover
        object-position: top
        width: 100%
        height: 400px

</style>