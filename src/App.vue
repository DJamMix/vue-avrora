<template>
  <nav class="nav">
    <div class="nav_blocklogo">
      <router-link to="/"><img src="./assets/img/logo.svg" alt="Логотип"></router-link>
    </div>
    <div class="nav_block-menu">
      <router-link to="/" class="nav_block-menu_item">Главная</router-link>
      <router-link to="/about" class="nav_block-menu_item">Правила</router-link>
    </div>
    <div class="nav_social-block">
      <a class="nav_social-block_item" href="#"><img src="./assets/img/icon-vk.svg" alt="Перейти в группу Вконтакте"></a>
      <a class="nav_social-block_item" href="#"><img src="./assets/img/icon-youtube.svg" alt="Перейти на канал Ютуб"></a>
      <a class="nav_social-block_item" href="#"><img src="./assets/img/icon-discord.svg" alt="Перейти в Discord"></a>
    </div>
    <div class="nav_pers-account-block">
      <a class="nav_pers-account-block_link" href="#">
        <img class="nav_pers-account-block_link_img" src="./assets/img/icon-lk.svg" alt="Личный кабинет">
        <p class="nav_pers-account-block_link_content">Личный кабинет</p>
      </a>
    </div>
  </nav>
  <router-view/>
</template>

<style>
  @import "assets/css/style.css";
</style>
