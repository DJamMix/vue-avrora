<template>
  <nav class="nav">
    <div class="nav_blocklogo">
      <router-link to="/"><img src="./assets/img/logo.svg" alt="Логотип"></router-link>
    </div>
    <div class="nav_block-menu">
      <router-link active-class="nav_block-menu_item-active" to="/" class="nav_block-menu_item">Главная</router-link>
      <router-link active-class="nav_block-menu_item-active" to="/about" class="nav_block-menu_item">Правила</router-link>
    </div>
    <div class="nav_social-block">
      <a class="nav_social-block_item" href="https://vk.com/nether_studio"><img src="./assets/img/icon-vk.svg" alt="Перейти в группу Вконтакте"></a>
      <a class="nav_social-block_item" href="#"><img src="./assets/img/icon-youtube.svg" alt="Перейти на канал Ютуб"></a>
      <a class="nav_social-block_item" href="#"><img src="./assets/img/icon-discord.svg" alt="Перейти в Discord"></a>
    </div>
    <div class="nav_pers-account-block">
      <a class="nav_pers-account-block_link" href="#">
        <img class="nav_pers-account-block_link_img" src="./assets/img/icon-lk.svg" alt="Личный кабинет">
        <p class="nav_pers-account-block_link_content">Личный кабинет</p>
      </a>
    </div>
    <div class="nav_menu">
      <div class="nav_menu_burger">
        <input id="toggle" type="checkbox" />
        <label class="nav_menu_burger_btn" for="toggle">
          <span></span>
        </label>
        <div class="nav_menu_burger_box">
          <a class="nav_menu_burger_box_item" href="#">Услуги</a>
          <a class="nav_menu_burger_box_item" href="#">Правила</a>
          <div class="nav_menu_burger_box_social">
            <a class="nav_menu_burger_box_social_icon" href="https://vk.com/nether_studio" target="blank"><img class="nav_menu_burger_box_social_icon_image" src="./assets/img/icon-vk.svg" alt=""></a>
            <a class="nav_menu_burger_box_social_icon" href="#" target="blank"><img class="nav_menu_burger_box_social_icon_image" src="./assets/img/icon-youtube.svg" alt=""></a>
            <a class="nav_menu_burger_box_social_icon" href="#" target="blank"><img class="nav_menu_burger_box_social_icon_image" src="./assets/img/icon-discord.svg" alt=""></a> 
          </div>
        </div>
      </div>
    </div>
    <div class="nav_background-burger"></div>
  </nav>
  <body>
    <main>

      <router-view/>
      
    </main>
  </body>
  <div class="black-footer">
    <footer class="footer">
      <div class="footer_blocklogo">
        <router-link to="/"><img src="./assets/img/logo-gray.svg" alt="Логотип"></router-link>
      </div>
      <div class="footer_block-menu">
        <router-link active-class="footer_block-menu_item-active" to="/" class="footer_block-menu_item">Главная</router-link>
        <router-link active-class="footer_block-menu_item-active" to="/about" class="footer_block-menu_item">Правила</router-link>
      </div>
      <div class="footer_social-block">
        <a class="footer_social-block_item" href="https://vk.com/nether_studio"><img src="./assets/img/icon-vk-gray.svg" alt="Перейти в группу Вконтакте"></a>
        <a class="footer_social-block_item" href="#"><img src="./assets/img/icon-youtube-gray.svg" alt="Перейти на канал Ютуб"></a>
        <a class="footer_social-block_item" href="#"><img src="./assets/img/icon-discord-gray.svg" alt="Перейти в Discord"></a>
      </div>
      <div class="footer_creators">
        <p class="footer_creators_text">Разработка сайта</p>
        <a class="footer_creators_link" href="https://vk.com/nether_studio">Nether Studio</a>
      </div> 
    </footer>
  </div>
</template>

<script>
import Banner from './components/Main/Banner.vue'

export default {
  components: {
    Banner,
  },
}
</script>

<style lang="sass" scoped>
@import "assets/css/style.css"
.nav
  &_menu
    display: none
    &_burger
      #toggle
        display: none
      #toggle:checked ~ &_btn > span
        transform: rotate(45deg)
      #toggle:checked ~ &_btn > span::before
        top: 0
        transform: rotate(0)
      #toggle:checked ~ &_btn > span::after
        top: 0
        transform: rotate(90deg)
      #toggle:checked ~ &_box
        visibility: visible
        top: 98px
        display: block
        border-radius: 0 0 25px 25px
        border-bottom: 2px solid
        border-color: #C5C5C5
      &_btn
        display: flex
        align-items: center
        position: relative
        width: 26px
        cursor: pointer
        z-index: 1
      &_btn > span,
      &_btn > span::before,
      &_btn > span::after
        display: block
        position: relative
        width: 100%
        height: 2px
        background-color: #000
        transition-duration: .25s
      &_btn > span::before
        content: ''
        top: -8px
      &_btn > span::after
        content: ''
        top: 8px
      &_box
        display: none
        position: fixed
        visibility: hidden
        left: 0
        top: -100%
        width: 100%
        margin: 0
        padding-top: 10px
        padding-bottom: 40px
        list-style: none
        background-color: #fff
        transition-duration: .25s
        &_item
          display: block
          padding: 25px 15px 30px
          color: #4A4A4A
          text-align: center
          font-size: 17px
          font-family: 'Montserrat-medium'
          text-decoration: none
          transition-duration: .25s
        &_social
          margin-top: 10px
          display: flex
          flex-direction: column
          align-items: center
          align-content: center
          justify-content: center
          &_icon
            margin: 15px
        &_li
          display: block
  &_background-burger
    display: none
    padding: 20px
    position: absolute
    background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
    right: 39px
//Адаптив
@media (max-width: 1200px) 
  .nav
    padding-left: 15px
    padding-right: 15px

  .footer
    padding-left: 15px
    padding-right: 15px

@media (max-width: 850px)
    .nav
      position: fixed
      height: 98px
      width: 100%
      top: 0
      align-items: center
      background: #fff
      &_background-burger
        display: block
      &_block-menu, &_social-block, &_pers-account-block_link
        display: none
      &_menu
        padding-right: 30px
        display: block
    .footer
      &_block-menu, &_social-block
        display: none
      &_creators
        &_text, &_link
          font-size: 15px

@media (max-width: 440px)
    .footer
        flex-direction: column
        justify-content: space-evenly
</style>
