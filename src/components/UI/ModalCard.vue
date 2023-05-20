<template>
    <div class="modal-card" v-if="show" @click="hideModal">
        <div @click.stop class="modal-card__content">
            <img :src="card.thumb" alt="">
            <h4 class="title">{{ card.series }}</h4>
            <h5 class="price">Price: {{ card.price }}
                <button class="btn-buy">BUY <i class="fa-solid fa-cart-shopping"></i></button>
            </h5>
        </div>
    </div>
</template>

<script>
export default {
    name: "CardModal",
    props: {
        show: {
            type: Boolean,
            default: false
        },
        card: {
            type: Object,
            required: true
        }
    },
    methods: {
        hideModal() {
            this.$emit('update:show', false)
        }
    }

}
</script>

<style lang="sass" scoped>

$modal-padding: 25px

.modal-card
    z-index: 99
    top: 0
    bottom: 0
    right: 0
    left: 0
    background: rgba(0, 0, 0, .65)
    position: fixed
    display: flex


    .modal-card__content
        position: relative
        margin: auto
        background: rgba(255, 255, 255, 0.75)
        border-radius: 12px
        width: 450px
        padding: $modal-padding
        display: flex
        flex-direction: column
        justify-content: space-between
        gap: 20px

        img
            height: calc(100% - $modal-padding)
            object-fit: cover

    .title
        text-align: center
        font-size: 20px
        font-weight: bold

    .price
        text-align: center
        font-size: 15px
        font-style: italic
        color: #1b71e6

        .btn-buy
            cursor: pointer
            padding: 8px
            font-weight: bold
            color: white
            background-color: rgba(10, 123, 234, 0.7)
            outline: none
            border: none
            border-radius: 5px
            margin-left: 10px
            transition: .3s

            &:hover
                background-color: rgb(10, 123, 234)

</style>