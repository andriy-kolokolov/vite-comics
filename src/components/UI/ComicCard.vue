<template>
    <div class="card-wrapper">
        <img :src="src" alt="comic card" class="card-img">
        <div class="title">{{ cardTitle.toUpperCase() }}</div>
    </div>
</template>

<script>
export default {
    name: "ComicCard",
    props: {
        src: {
            type: String,
            required: true
        },
        cardTitle: {
            type: String,
            required: true
        }

    }
}
</script>

<style lang="sass" scoped>
$card-transition: .3s

.card-wrapper:hover
    .card-img
        scale: 1.15

    .title
        color: #0a7bea

.card-img
    cursor: pointer
    width: 100%
    aspect-ratio: 1 / 1
    object-fit: cover
    object-position: top
    transition: $card-transition

    &:hover
        scale: 1.15

.title
    text-align: center
    font-weight: bold
    margin-top: 20px
    color: white
    font-size: 13px
    transition: $card-transition

</style>