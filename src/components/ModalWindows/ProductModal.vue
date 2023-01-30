<template>
    <div v-if="visible" class="ProductModalShadow" id="shadowModal" @click.self="closeModal">
        <div class="ProductModal">
            <button class="ProductModal_close" @click.self="closeModal">&#10006;</button>
            <div class="ProductModal_header">
                <img class="ProductModal_header_img" :src="Product.img" alt="Товар">
                <h1 class="ProductModal_header_productName">{{Product.name}}</h1>
            </div>
            <div class="ProductModal_body">
                <div class="ProductModal_body_block">
                    <h2 class="ProductModal_body_block_title">Описание возможностей</h2>
                    <p class="ProductModal_body_block_text" v-for="descrip in Product.description" :key="descrip.item">{{ descrip.item }}</p>
                </div>
                <div class="ProductModal_body_block">
                    <h2 class="ProductModal_body_block_title">Дополнительно</h2>
                    <p class="ProductModal_body_block_text" v-for="addition in Product.additionally" :key="addition.item">{{ addition.item }}</p>
                </div>
            </div>
            <form class="ProductModal_footer">
                <input type="text" placeholder="Введите ваш ник">
                <div class="ProductModal_footer_button">
                    <button>
                        Купить
                    </button>
                    <p>
                        {{ Product.price }} руб.
                        <span>
                            Навсегда
                        </span>
                    </p>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductModal',
    props: {
        Product: {
            type: Object,
            default: {
                id: 1,
                name: 'ERROR',
                img: "/img/img-vip.9120969a.png",
                price: 'ERROR',
                category: 'privilegesItem',
            },
        },
        visible: {
            type: Boolean,
            default: false
        },
    },
    methods: {
        closeModal: function () {
            this.$emit('closeModal',false)
            document.getElementById('shadowModal').style.opacity = 0
        },
    }
    
}
</script>

<style lang="sass" scoped>
    .ProductModalShadow
        position: fixed
        z-index: 9999
        top: 0
        left: 0
        width: 100%
        height: 100%
        background-color: rgba(0, 0, 0, 0.5)
        transition: 0.3s
        opacity: 0
    .ProductModal
        background-color: white
        min-width: 775px
        position: absolute
        top: 50%
        left: 50%
        transform: translate(-50%, -50%)
        padding: 40px 70px
        border-radius: 35px
        &_close
            border: none
            outline: none
            background: none
            font-size: 30px
            display: flex
            width: 100%
            justify-content: flex-end
            cursor: pointer
            transition: 0.2s
        &_close:active,
        &_close:hover
            opacity: 0.5
        &_header
            display: flex
            align-items: center
            margin-top: -35px
            &_img
                min-width: 216px
                min-height: 163px
            &_productName
                font-family: "Montserrat-bold"
                font-style: normal
                font-weight: 700
                font-size: 40px
                line-height: 49px
                width: 344px
                text-align: center
                text-transform: uppercase
        &_body
            padding-left: 41px
            padding-right: 41px
            &_block
                margin-top: 40px
                &_title
                    font-weight: 600
                    font-size: 25px
                    line-height: 30px
                    text-transform: uppercase
                    color: #000000
                    text-align: center
                    font-family: Montserrat-regular
                    margin-bottom: 40px
                &_text
                    font-weight: 400
                    font-size: 22px
                    line-height: 27px
                    color: #000000
                    font-family: Montserrat-regular
                    margin-top: 7.5px
                    margin-bottom: 7.5px
        &_footer
            padding-left: 41px
            padding-right: 41px
            margin-top: 60px
            input
                padding: 24px 30px
                background: #F3F3F3
                border: none
                outline: none
                font-weight: 500
                font-size: 19px
                line-height: 23px
                border-radius: 10px
                color: rgba(0, 0, 0, 0.4)
                min-width: 402px
            &_button
                margin-top: 36px
                display: flex
                flex-direction: row
                align-items: center
                button
                    border: none
                    outline: none
                    background: linear-gradient(108.02deg, #FFDD00 -17.78%, #FBB034 129.91%)
                    border-radius: 10px
                    font-weight: 600
                    font-size: 20px
                    line-height: 24px
                    color: #000000
                    padding: 24px 83px
                    cursor: pointer
                    font-family: "Montserrat-bold"
                    transition: 0.2s
                button:active,
                button:hover
                    opacity: 0.7
                p
                    margin-left: 55px
                    font-family: "Montserrat-bold"
                    color: #000000
                    font-weight: 600
                    font-size: 22px
                    line-height: 27px
                    display: flex
                    flex-direction: column
                    span
                        font-family: Montserrat-regular
                        font-weight: 600
                        font-size: 15px
                        line-height: 18px
                        color: rgba(0, 0, 0, 0.4)
                        text-transform: uppercase
@media (max-width: 900px)
    .ProductModal
        min-width: auto
        &_header
            &_productName
                text-align: left
@media (max-width: 700px)
    .ProductModal
        max-width: 315px
        padding: 15px 30px
        &_close
            display: none
        &_header
            display: flex
            flex-direction: column
            justify-content: center
            margin-top: 29px
            &_img
                width: 163px
                height: 123px
            &_productName
                width: auto
                margin-top: 12px
                font-size: 25px
                line-height: 21px
        &_body
            padding: 0px
            &_block
                margin-top: 25px
                &_title
                    font-size: 12px
                    line-height: 15px
                    margin-bottom: 25px
                &_text
                    font-size: 12px
                    line-height: 15px
        &_footer
            padding: 0px
            margin-top: 26px
            input
                min-width: 172px
                padding: 10px 10px
                border-radius: 0px
                font-size: 12px
            &_button
                margin-top: 32px
                button
                    padding: 10px 28px
                    font-size: 12px
                    line-height: 15px
                p
                    font-size: 12px
                    line-height: 15px
                    margin-left: 20px
                    span
                        font-size: 12px
                        line-height: 15px
</style>