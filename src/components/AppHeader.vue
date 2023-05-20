<link rel="stylesheet" href="../assets/styles/main.sass">
<template>
    <div class="header-wrapper">
        <div class="container">
            <div class="header__logo">
                <a href="#"><img src="../../public/img/dc-logo.png" alt="logo img"/></a>
            </div>
            <nav class="navbar">
                <ul class="nav-list">
                    <li @click="setActive(index)" v-for="(link, index) in navLinks" :key="index" :class="{'nav-item': true, 'active': index === activeLink}">
                        <a :href="link.url">{{ link.name }}</a>
                    </li>
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
    name: "AppHeader",
    data() {
        return {
            navLinks: [
                { name: "CHARACTERS", url: "#" },
                { name: "COMICS", url: "#" },
                { name: "MOVIES", url: "#" },
                { name: "TV", url: "#" },
                { name: "GAMES", url: "#" },
                { name: "COLLECTIBLES", url: "#" },
                { name: "VIDEOS", url: "#" },
                { name: "FANS", url: "#" },
                { name: "NEWS", url: "#" },
                { name: "SHOP", url: "#" }
            ],
            activeLink: 1
        };
    },
    methods: {
        setActive(index) {
            this.activeLink = index;
        }
    }
}
</script>

<style lang="sass" scoped>
@import "src/assets/styles/partials/variables"

.container
    display: flex
    justify-content: space-between

    .header__logo
        padding: 20px 0

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

                &.active
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