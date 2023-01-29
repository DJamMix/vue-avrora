<template>
    <section class="banner">
        <div class="banner_banner-block">
            <div class="banner_banner-block_text-and-button">
                <h1>Начни свой новый путь во влесенной легендарного Minecraft</h1>
                <button @click="showStartPlayModal">Начать играть</button>
            </div>
            <div class="banner_banner-block_online-players">
                <h2>Онлайн</h2>
                <p>0/0 игроков</p>
            </div>
        </div>

        <StartPlayModal ref="modal"></StartPlayModal>
    </section>
</template>

<script>
import StartPlayModal from '../ModalWindows/StartPlayModal.vue';

export default {
    name: 'Banner',
    components: {
        StartPlayModal,
    },
    methods: {
        showStartPlayModal: function () {
            this.$refs.modal.show = true

            setTimeout(() => {
                document.getElementById('shadowModal').style.opacity = 1
            }, 100)
        }
    }
}
</script>

<style lang="sass" scoped>
    .banner
        background-color: #F3F3F3
        padding-top: 88px
        padding-bottom: 66px
        &_banner-block
            background-image: url(../../assets/img/banner-background.png)
            max-width: 1170px
            border-radius: 35px
            background-size: 100% 330px
            margin: auto
            display: flex
            justify-content: space-around
            align-items: center
            height: 330px
            &_text-and-button
                h1
                    font-weight: 700
                    font-size: 30px
                    line-height: 110%
                    color: #FFFFFF
                    text-transform: uppercase
                    font-family: 'Montserrat-bold'
                    max-width: 563px
                button
                    margin-top: 18px
                    font-weight: 600
                    font-size: 15px
                    line-height: 100.4%
                    border: 1px solid white
                    border-radius: 10px
                    background: none
                    color: white
                    font-family: 'Montserrat-regular'
                    text-transform: uppercase
                    padding: 12px
                    cursor: pointer
                    padding-left: 22px
                    padding-right: 22px
                    transition: 0.2s
                button:active,
                button:hover
                    border: 1px solid black
                    background-color: white
                    color: black
                    transition: 0.2s

            &_online-players
                text-align: center
                h2
                    font-weight: 700
                    font-size: 24px
                    line-height: 110%
                    font-family: 'Montserrat-bold'
                    text-transform: uppercase
                    color: #FFFFFF
                p
                    font-weight: 600
                    font-size: 12px
                    line-height: 110%
                    text-transform: uppercase
                    font-family: 'Montserrat-regular'
                    color: #FFFFFF
                    margin-top: 5px

//Адаптив
@media (max-width: 1200px)
    .banner
        padding-left: 15px
        padding-right: 15px
                
@media (max-width: 850px)
    .banner
        padding: 0
        &_banner-block
            padding-left: 15px
            padding-right: 15px
            background-size: cover
            border-radius: 0px
            
@media (max-width: 680px)
    .banner
        &_banner-block
            &_text-and-button
                h1
                    max-width: none
            &_online-players
                display: none

@media (max-width: 615px)
    .banner
        &_banner-block
            justify-content: initial
            &_text-and-button
                h1
                    font-size: 25px
                    width: 394px
                button
                    font-size: 10px

@media (max-width: 440px)
    .banner
        &_banner-block
            &_text-and-button
                h1
                    width: auto

</style>