<template>
    <div class="main-wrapper">
        <div class="container">
            <div class="title">
                <h1>CURRENT SERIES</h1>
            </div>

            <div class="cards">
                <comic-card
                        v-for="(card, index) in cardsData"
                        :key="index"
                        :src="card.thumb"
                        :card-title="card.series"/>
            </div>
        </div>
    </div>
</template>

<script>
import cardsDataJson from '../../public/dc-comics.json'
import {ComicCard} from "./UI/index.js";

export default {
    components: {ComicCard},
    data() {
        return {
            cardsData: cardsDataJson
        }
    },
    name: "AppMain"
}
</script>

<style lang="sass" scoped>
@import "src/assets/styles/partials/variables"
@keyframes pulse
    0%
        opacity: 1
        transform: scale(1)
    50%
        opacity: 0.7
        transform: scale(1.2)
    100%
        opacity: 1
        transform: scale(1)

.main-wrapper
    $container-padding: 70px
    $grid-cols: 6
    $grid-gap: 40px

    background-color: #1c1c1c

    .container
        position: relative
        padding: $container-padding

        .title
            cursor: default
            width: fit-content
            padding: 10px
            background-color: #0282f9
            color: white
            position: absolute
            top: calc($container-padding * -1 / 2)
            //transform: translate(0, calc(-50% - $container-padding))
            animation: pulse 1.5s infinite

        .cards
            display: grid
            grid-template-columns: repeat($grid-cols, 1fr)
            gap: $grid-gap
</style>