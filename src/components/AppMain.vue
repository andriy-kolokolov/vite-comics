<template>
    <div class="main-wrapper">
        <div class="container">

            <div class="title">
                <h1>CURRENT SERIES</h1>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "AppMain"
}
</script>

<style lang="sass" scoped>
@import "src/assets/styles/partials/variables"
.main-wrapper
    $container-padding: 15px

    background-color: #1c1c1c
    height: 400px

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
            transform: translate(0, calc(-50% - $container-padding))

</style>