<template>
    <section class="catalog">
        <div class="catalog_block">
            <div class="catalog_block_nav">
                <button>Привилегии</button>
                <button class="catalog_block_nav_btn" id="case">Кейсы</button>
                <button class="catalog_block_nav_btn" id="titles">Титулы</button>
                <button class="catalog_block_nav_btn">Прочее</button>
            </div>
        </div>
        <div class="catalog_listen">
            <div class="catalog_listen_items">
                <div class="catalog_listen_items_product">
                    <p class="catalog_listen_items_product_name">Vip</p>
                    <img class="catalog_listen_items_product_image" src="../../assets/img/img-vip.png" alt="#">
                    <p class="catalog_listen_items_product_price">35 руб.</p>
                    <p class="catalog_listen_items_product_info">подробнее</p>
                </div>
            </div>
            <div class="catalog_listen_items">
                <div class="catalog_listen_items_product">
                    <p class="catalog_listen_items_product_name">Premium</p>
                    <img class="catalog_listen_items_product_image" src="../../assets/img/img-premium.png" alt="#">
                    <p class="catalog_listen_items_product_price">70 руб.</p>
                    <p class="catalog_listen_items_product_info">подробнее</p>
                </div>
            </div>
            <div class="catalog_listen_items">
                <div class="catalog_listen_items_product">
                    <p class="catalog_listen_items_product_name">Creative</p>
                    <img class="catalog_listen_items_product_image" src="../../assets/img/img-creative.png" alt="#">
                    <p class="catalog_listen_items_product_price">95 руб.</p>
                    <p class="catalog_listen_items_product_info">подробнее</p>
                </div>
            </div>
            <div class="catalog_listen_items">
                <div class="catalog_listen_items_product">
                    <p class="catalog_listen_items_product_name">Admin</p>
                    <img class="catalog_listen_items_product_image" src="../../assets/img/img-admin.png" alt="#">
                    <p class="catalog_listen_items_product_price">120 руб.</p>
                    <p class="catalog_listen_items_product_info">подробнее</p>
                </div>
            </div>
        </div>
    </section>
  </template>
  
  <script>
  
  export default {
    name: 'Catalog',
    components: {
    }
  }
  </script>

<style lang="sass" scoped>
    .catalog
        background-color: #F3F3F3
        padding-bottom: 80px
        &_block
            background: #fff
            height: 118px
            &_nav
                margin: auto
                text-align: center
                button
                    background: #fff
                    font-size: 15px
                    border: none
                    font-family: 'Montserrat-medium'
                    padding-bottom: 44px
                    padding-top: 44px
                    transition: 0.2s
                    margin-right: 40px
                    margin-left: 40px
                    cursor: pointer
                button:hover
                    border-bottom: 11px solid 
                    border-image-source: linear-gradient(90deg, #FFDD00, #FBB034)
                    border-image-slice: 1
                    transition: 0.2s
                &_btn
                    margin-left: 80px
        &_listen
            max-width: 1170px
            display: flex
            flex-wrap: wrap
            margin: 0 auto
            &_items
                margin: 0 auto
                margin-top: 40px
                max-width: 1170px
                display: flex
                &_product
                    background: #fff
                    width: 270px
                    height: 270px
                    display: flex
                    align-items: center
                    flex-direction: column
                    &_name
                        font-size: 20px
                        font-family: 'Montserrat-bold'
                        margin-top: 20px
                        text-align: center
                    &_image
                        display: block
                        margin-top: 17px
                    &_price
                        font-size: 16px
                        text-align: center
                        margin-top: 207px
                        position: absolute
                        font-family: 'Montserrat-bold'
                        background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
                        padding: 5px 10px
                    &_info
                        font-family: 'Montserrat-regular'
                        font-size: 12px
                        text-transform: uppercase
                        display: none

//Адаптив                
@media (max-width: 850px)
    .catalog
        &_listen
            padding-left: 20px
            padding-right: 20px
                
@media (max-width: 605px)
    .catalog
        &_block
            &_nav
                #titles
                    display: none
        &_listen
            &_items
                &_product
                    width: 450px
                    height: 150px
                    display: flex
                    align-items: center
                    flex-direction: row
                    justify-content: space-between
                    padding-left: 15px
                    padding-right: 15px
                    &_name
                        margin-top: -30px
                        margin-left: 175px
                    &_image
                        margin-top: 0px
                        position: absolute
                        order: -1
                        width: 155px
                    &_price
                        margin-top: 32px
                        margin-left: 175px
                    &_info
                        display: block

@media (max-width: 520px)
    .catalog
        &_block
            display: block
            &_nav
                #case
                    display: none
        &_listen
            display: block

@media (max-width: 440px)
    .catalog
        &_listen
            &_items
                &_product
                    &_info
                        display: none

@media (max-width: 350px)
    .catalog
        &_listen
            &_items
                &_product
                    &_name
                        margin-left: 150px
                    &_price
                        margin-left: 150px
                    &_image
                        margin-left: -15px
</style>

