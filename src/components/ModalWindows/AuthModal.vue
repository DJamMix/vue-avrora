<template>
    <div v-if="show" class="AuthModal" id="ShowAuthModal" @click.self="closeModal">
        <form class="AuthModal_form">
            <p class="AuthModal_form_title">Авторизация</p>
            <input type="text" placeholder="Имя пользователя">
            <input type="text" placeholder="Пароль">
            <button>Войти</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'AuthModal',
    components: {

    },
    data: function () {
        return {
            show: false
        }
    },
    methods: {
        closeModal: function () {
            document.getElementById('ShowAuthModal').style.opacity = 0

            setTimeout(() => {
                this.show = false
            }, 100)
        },
    }
}
</script>

<style lang="sass" scoped>
.AuthModal
    position: fixed
    z-index: 9999
    top: 0
    left: 0
    width: 100%
    height: 100%
    background-color: rgba(0, 0, 0, 0.5)
    display: table
    transition: 0.3s
    opacity: 0
    &_form
        background: #FFFFFF
        border-radius: 35px
        min-width: 615px
        position: absolute
        top: 50%
        left: 50%
        transform: translate(-50%, -50%)
        display: flex
        flex-direction: column
        justify-content: center
        align-items: center
        &_title
            font-weight: 700
            font-size: 40px
            line-height: 49px
            color: #000000
            font-family: "Montserrat-bold"
            text-align: center
            margin-top: 123px
            margin-bottom: 52.5px
        input
            padding: 25px 30px
            background: #F3F3F3
            border-radius: 10px
            outline: none
            border: none
            color: rgba(0, 0, 0, 0.4)
            min-width: 462px
            font-family: Montserrat-regular
            margin-top: 12.5px
            margin-bottom: 12.5px
        button
            border: none
            output: none
            cursor: pointer
            background: linear-gradient(108.02deg, #FFDD00 -17.78%, #FBB034 129.91%)
            border-radius: 10px
            padding: 24px 88px
            font-weight: 600
            font-size: 20px
            line-height: 24px
            color: #000000
            font-family: "Montserrat-bold"
            margin-top: 36.5px
            margin-bottom: 123px
            transition: 0.2s
        button:active,
        button:hover
            opacity: 0.8
</style>