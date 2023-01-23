<template>
    <section class="panel">
        <div class="panel_block">
            <h1>админ панель</h1>
            <div class="panel_block_objects">
                <div class="panel_block_objects_product">
                    <div class="panel_block_objects_product_inside">
                        <p class="panel_block_objects_product_inside_header">Тип товара</p>
                        <button class="panel_block_objects_product_inside_btn">Привилегии</button>
                        <button class="panel_block_objects_product_inside_btn">Кейсы</button>
                        <button class="panel_block_objects_product_inside_btn">Титулы</button>
                        <button class="panel_block_objects_product_inside_btn">Прочее</button>
                        <p class="panel_block_objects_product_inside_header">Название товара</p>
                        <input type="text" placeholder="Введите название товара">
                        <p class="panel_block_objects_product_inside_header">Описание товара</p>
                        <input type="text" placeholder="Сражайся до последнего!">
                        <p class="panel_block_objects_product_inside_header">Команды для выдачи</p>
                        <input type="text" placeholder="Введите команду для выдачи">
                        <p class="panel_block_objects_product_inside_header">Изображение товара</p>
                        <div class="panel_block_objects_product_inside_image">
                            <img class="panel_block_objects_product_inside_image_img" src="../../assets/img/icon-product.png" alt="Сменить иконку">
                            <button class="panel_block_objects_product_inside_image_btn-img">Изменить</button>
                            <button class="panel_block_objects_product_inside_image_btn-img">Удалить</button>
                        </div>
                        <p class="panel_block_objects_product_inside_header">Стоимость</p>
                        <input type="text" placeholder="Введите стоимость">
                        <div class="panel_block_objects_product_inside_add-item">
                            <a class="panel_block_objects_product_inside_add-item_button">
                                <img class="panel_block_objects_product_inside_add-item_button_img" src="../../assets/img/icon-additem.svg" alt="Личный кабинет">
                                <p class="panel_block_objects_product_inside_add-item_button_text">Добавить товар</p>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="panel_block_objects_works">
                    <div class="panel_block_objects_works_item">
                        <p>В разработке</p>
                    </div>
                    <div class="panel_block_objects_works_item">
                        <p>В разработке</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="panel_catalog">
            <h1>Каталог товаров</h1>
            <div class="panel_catalog_listen">
                <div class="panel_catalog_listen_items">
                    <div class="panel_catalog_listen_items_product">
                        <p class="panel_catalog_listen_items_product_name">Vip</p>
                        <img class="panel_catalog_listen_items_product_image" src="../../assets/img/img-vip.png" alt="#">
                        <p class="panel_catalog_listen_items_product_price">35 руб.</p>
                        <p class="panel_catalog_listen_items_product_info">подробнее</p>
                    </div>
                </div>
                <div class="panel_catalog_listen_items">
                    <div class="panel_catalog_listen_items_product">
                        <p class="panel_catalog_listen_items_product_name">Premium</p>
                        <img class="panel_catalog_listen_items_product_image" src="../../assets/img/img-premium.png" alt="#">
                        <p class="panel_catalog_listen_items_product_price">70 руб.</p>
                        <p class="panel_catalog_listen_items_product_info">подробнее</p>
                    </div>
                </div>
                <div class="panel_catalog_listen_items">
                    <div class="panel_catalog_listen_items_product">
                        <p class="panel_catalog_listen_items_product_name">Creative</p>
                        <img class="panel_catalog_listen_items_product_image" src="../../assets/img/img-creative.png" alt="#">
                        <p class="panel_catalog_listen_items_product_price">95 руб.</p>
                        <p class="panel_catalog_listen_items_product_info">подробнее</p>
                    </div>
                </div>
                <div class="panel_catalog_listen_items">
                    <div class="panel_catalog_listen_items_product">
                        <p class="panel_catalog_listen_items_product_name">Admin</p>
                        <img class="panel_catalog_listen_items_product_image" src="../../assets/img/img-admin.png" alt="#">
                        <p class="panel_catalog_listen_items_product_price">120 руб.</p>
                        <p class="panel_catalog_listen_items_product_info">подробнее</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Panel',
    components: {
  }
}
</script>

<style lang="sass" scoped>

    .panel
        max-width: 1170px
        margin: 0 auto
        padding-bottom: 100px
        &_block
            padding-top: 75px
            h1
                text-transform: uppercase
                font-size: 25px
                text-align: center
                font-family: 'Montserrat-extrabold'
            &_objects
                max-width: 1170px
                padding-top: 55px
                display: flex
                &_product
                    width: 485px
                    padding-bottom: 40px
                    background: #fff
                    &_inside
                        margin-left: 30px
                        text-align: left
                        &_header
                            font-family: 'Montserrat-bold'
                            font-size: 22px
                            margin-top: 38px
                            color: #718096
                        &_btn
                            margin-top: 15px
                            font-size: 17px
                            background: #EFF2F7
                            padding: 7px 7px
                            border: none
                            font-family: 'Montserrat-medium'
                            transition: 0.2s
                            margin-left: 5px
                            margin-right: 5px
                            cursor: pointer
                        &_btn:focus
                            background: linear-gradient(90deg, #FFDD00, #FBB034)
                            transition: 0.2s
                            font-family: 'Montserrat-bold'
                        input
                            border: none
                            outline: none
                            width: 260px
                            font-size: 16px
                            margin-top: 10px
                            font-family: 'Montserrat-regular'
                        &_image
                            display: flex
                            align-content: flex-start
                            align-items: flex-start
                            margin-top: 10px
                            &_btn-img
                                font-family: 'Montserrat-regular'
                                margin-top: 7px
                                border: none
                                color: #A0AEC0
                                background: none
                                margin-left: 25px
                                font-size: 16px
                                cursor: pointer
                        &_add-item
                            padding-top: 40px
                            &_button
                                background-color: #1BD850
                                display: flex
                                width: 195px
                                flex-direction: row
                                text-decoration: none
                                align-items: center
                                transition: 0.2s
                                cursor: pointer
                                &_img
                                    padding: 10px
                                    background-color: #35CD5F
                                &_text
                                    font-weight: 600
                                    font-size: 15px
                                    line-height: 18px
                                    color: #FFFFFF
                                    font-family: 'Montserrat-regular'
                                    text-align: center
                                    margin-left: 14px
                &_works
                    justify-content: space-between
                    display: flex
                    flex-direction: column
                    &_item
                        width: 682px
                        height: 360px
                        background: #fff
                        align-items: center
                        display: flex
                        justify-content: center
                        margin-left: 40px
                        p
                            text-transform: uppercase
                            text-align: center
                            color: #A0AEC0
                            font-size: 17px
                            font-family: 'Montserrat-bold'
        &_catalog
            padding-top: 40px
            padding-bottom: 40px
            h1
                text-transform: uppercase
                font-size: 25px
                text-align: center
                font-family: 'Montserrat-extrabold'
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
@media (max-width: 1200px)                          
    .panel
        &_block
            &_objects
                flex-wrap: wrap
                flex-direction: column
                &_product
                    display: flex
                    margin: auto
                &_works
                    margin: auto
                    margin-top: 10px
                    &_item
                        margin-left: 0px
                        margin-top: 30px
@media (max-width: 720px) 
    .panel
        &_block
            &_objects
                &_works
                    display: flex
                    margin: none
                    align-items: center
                    margin: 0
                    padding: 0 20px
                    &_item
                        width: 100%
                        max-width: 682px
@media (max-width: 560px) 
    .panel
        &_block
            h1
                font-size: 20px
        &_catalog
            h1
                font-size: 20px
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
@media (max-width: 560px)
    .panel
        &_block
            &_objects
                p,input,button
                    font-size: 16px
        &_catalog
            &_listen
                max-width: 450px
                width: 100%
                display: block
                &_items
                    padding: 0 20px
@media (max-width: 525px)
    .panel
        &_block
            &_objects
                &_product
                    width: 100%
                    &_inside
                        margin-left: 50px
                &_works
                    padding: 0

@media (max-width: 420px)
    .panel
        &_block
            &_objects
                &_product
                    &_inside
                        margin-left: 40px
        &_catalog
            &_listen
                &_items
                    &_product
                        &_info
                            display: none
</style>