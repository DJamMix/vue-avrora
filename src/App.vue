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
      <router-link class="nav_pers-account-block_link" to="/auth">
        <img class="nav_pers-account-block_link_img" src="./assets/img/icon-lk.svg" alt="Личный кабинет">
        <p class="nav_pers-account-block_link_content">Личный кабинет</p>
      </router-link>
    </div>
  </nav>
  <body>

    <router-view/>

  </body>
  <div class="black-footer">
    <footer class="footer">
      <div class="footer_blocklogo">
        <router-link to="/"><img src="./assets/img/logo-gray.svg" alt="Логотип"></router-link>
      </div>
      <div class="footer-block-menu">
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
    Banner
  },
}
</script>

<style>
  @import "assets/css/style.css";
</style>
