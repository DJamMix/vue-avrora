<template>
    <div v-if="show" class="StartPlayModalShadow" id="shadowModal" @click.self="closeModal">
        <div class="StartPlayModal">
            <div class="StartPlayModal_close" @click="closeModal">&#10006;</div>
            <div class="StartPlayModal_title">
                <slot name="Header-modal">
                    <h3 class="StartPlayModal_title_text">Привет! Вот наш IP сервера, подключайся и играй!</h3>
                </slot>
            </div>
            <div class="StartPlayModal_body">
                <slot name="Body-modal">
                    <div class="StartPlayModal_body_content">
                        <p>
                            Наш IP:
                            <input type="text" value="localhost:25565" id="inputCopy" readonly>
                        </p>
                    </div>
                </slot>
            </div>
            <div class="StartPlayModal_footer">
                <slot name="Footer-modal">
                    <div class="StartPlayModal_footer_content">
                        <button class="StartPlayModal_footer_content_button" id="copyButton" @click="copyIP">
                            Копировать
                        </button>
                    </div>
                </slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "StartPlayModal",
    data: function () {
        return {
            show: false
        }
    },
    methods: {
        closeModal: function () {
            document.getElementById('shadowModal').style.opacity = 0

            setTimeout(() => {
                this.show = false
            }, 100)
        },
        copyIP() {
            const inputCopy = document.getElementById('inputCopy')

            inputCopy.focus()

            document.execCommand('copy')

            setTimeout(() => {
                inputCopy.value = 'Скопировано!'
                inputCopy.style.color = 'black'
                inputCopy.style.backgroundColor = 'white'
            }, 100)

            setTimeout(() => {
                inputCopy.value = 'localhost:25565'
                inputCopy.style.color = 'white'
                inputCopy.style.background = 'none'
            }, 600)
        },
    }
}
</script>

<style lang="sass" scoped>
    .StartPlayModalShadow
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
    .StartPlayModal
        background-image: url(../../assets/img/banner-background.png)
        background-size: 100% 350px
        border-radius: 8px
        min-width: 40%
        position: absolute
        top: 50%
        left: 50%
        transform: translate(-50%, -50%)
        &_close
            display: flex
            justify-content: flex-end
            padding: 15px
            font-size: 20px
            cursor: pointer
            background-color: white
            border-radius: 8px 8px 0px 0px
        &_title
            margin-top: 50px
            margin-bottom: 50px
            height: 100px
            display: flex
            align-items: center
            padding-left: 20px
            padding-right: 20px
            &_text
                font-weight: 700
                font-size: 30px
                line-height: 110%
                color: white
                text-transform: uppercase
                font-family: "Montserrat-bold"
                text-align: center
        &_body
            margin-bottom: 50px
            &_content
                p
                    font-size: 20px
                    text-transform: uppercase
                    font-family: "Montserrat-bold"
                    text-align: center
                    color: white
                    input
                        border: 1px solid white
                        padding: 10px
                        border-radius: 10px
                        background: none
                        outline: none
                        font-size: 20px
                        font-family: "Montserrat-bold"
                        text-align: center
                        color: white
                        transition: 0.4s
        &_footer
            background-color: white
            font-size: 20px
            border-radius: 0px 0px 8px 8px
            &_content
                &_button
                    padding: 15px
                    border: none
                    outline: none
                    background: none
                    font-size: 20px
                    font-family: "Montserrat-bold"
                    text-align: center
                    color: black
                    cursor: pointer
                    width: 100%
                    transition: 0.2s
                &_button:active,
                &_button:hover
                    font-size: 23px
@media (max-width: 700px)
    .StartPlayModal
        padding: 10px
        &_title
            &_text
                font-size: 20px
        &_body
            &_content
                p
                    input
                        max-width: 210px
</style>