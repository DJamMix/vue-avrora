<template>
    <section class="catalog">
        <div class="catalog_catalog-block">
            <div class="catalog_catalog-block_nav">
                <button>Привилегии</button>
                <button class="catalog_catalog-block_nav_nav-button">Кейсы</button>
                <button class="catalog_catalog-block_nav_nav-button">Титулы</button>
                <button class="catalog_catalog-block_nav_nav-button">Прочее</button>
            </div>
        </div>
        <div class="catalog_catalog-listen">
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Vip</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-vip.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">35 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Premium</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-premium.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">70 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Creative</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-creative.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">95 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Admin</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-admin.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">120 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
        </div>
        <div class="catalog_catalog-listen">
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Vip</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-vip.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">35 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Premium</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-premium.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">70 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Creative</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-creative.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">95 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
                </div>
            </div>
            <div class="catalog_catalog-listen_catalog-items">
                <div class="catalog_catalog-listen_catalog-items_product">
                    <p class="catalog_catalog-listen_catalog-items_product_name">Admin</p>
                    <img class="catalog_catalog-listen_catalog-items_product_image" src="../../assets/img/img-admin.png" alt="#">
                    <div class="catalog_catalog-listen_catalog-items_product_object">
                    <p class="catalog_catalog-listen_catalog-items_product_price">120 руб.</p>
                    <div class="catalog_catalog-listen_catalog-items_product_rectangle"></div>
                    </div>
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
        &_catalog-block
            background: #fff
            height: 118px
            &_nav
                margin: auto
                display: flex
                justify-content: center
                align-items: flex-start
                button
                    background: #fff
                    font-size: 15px
                    border: none
                    font-family: 'Montserrat-medium'
                    padding-bottom: 44px
                    padding-top: 44px
                    transition: 0.2s
                    margin-right: 30px
                button:hover
                    border-bottom: 11px solid 
                    border-image-source: linear-gradient(90deg, #FFDD00, #FBB034)
                    border-image-slice: 1
                    transition: 0.2s
                &_nav-button
                    margin-left: 80px
        &_catalog-listen
            max-width: 1170px
            display: flex
            margin: 0 auto
            &_catalog-items
                margin: 0 auto
                margin-top: 40px
                max-width: 1170px
                display: flex
                &_product
                    background: #fff
                    width: 270px
                    height: 270px
                    &_name
                        font-size: 20px
                        font-family: 'Montserrat-bold'
                        margin-top: 20px
                        text-align: center
                    &_image
                        margin: 0 auto
                        display: block
                        margin-top: 17px
                    &_object
                        display: flex
                        align-items: center
                        justify-content: center
                        position: relative
                        margin-top: 17px
                    &_price
                        font-size: 16px
                        text-align: center
                        font-family: 'Montserrat-bold'
                        position: absolute
                    &_rectangle
                        background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
                        width: 118px
                        border-radius: 10px
                        height: 31px
</style>

