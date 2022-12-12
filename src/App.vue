<template>
  <nav class="nav">
    <div class="nav_blocklogo">
      <a href="#"><img src="./assets/img/logo.svg" alt="Логотип"></a>
    </div>
    <div class="nav_block-menu">
      <a class="nav_block-menu_item" href="#">Главная</a>
      <a class="nav_block-menu_item" href="#">Правила</a>
    </div>
    <div>
      <a href="#"><img src="./assets/img/icon-vk.svg" alt="Перейти в группу Вконтакте"></a>
      <a href="#"><img src="./assets/img/icon-youtube.svg" alt="Перейти на канал Ютуб"></a>
      <a href="#"><img src="./assets/img/icon-discord.svg" alt="Перейти в Discord"></a>
    </div>
    <div>
      <a href="#"><img src="./assets/img/icon-lk.svg" alt="Личный кабинет"><p>Личный кабинет</p></a>
    </div>
  </nav>
  <router-view/>
</template>

<style>
  @import "assets/css/style.css";
</style>
