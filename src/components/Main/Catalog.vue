<template>
    <section class="catalog">
        <div class="catalog_block">
            <div class="catalog_block_nav">
                <button @click="buttonCategory(filterCatalog.id)" class="catalog_block_nav_btn button-category" v-for="filterCatalog in filtersCatalog" :key="filterCatalog.id" :id="filterCatalog.id">{{ filterCatalog.name }}</button>
            </div>
        </div>
        <div class="catalog_listen">
            <div class="catalog_listen_items" :id="CatalogItem.category" v-for="CatalogItem in Products" :key="CatalogItem.id">
                <div class="catalog_listen_items_product" :id="CatalogItem.id" @click="showProductModal(CatalogItem)">
                    <img class="catalog_listen_items_product_image adaptiv" :src="CatalogItem.img" alt="Товар">
                    <p class="catalog_listen_items_product_name no-adaptiv">{{ CatalogItem.name }}</p>
                    <img class="catalog_listen_items_product_image no-adaptiv" :src="CatalogItem.img" alt="Товар">
                    <p class="catalog_listen_items_product_price no-adaptiv">{{ CatalogItem.price }} руб.</p>
                    <div>
                        <p class="catalog_listen_items_product_name adaptiv">{{ CatalogItem.name }}</p>
                        <p class="catalog_listen_items_product_price adaptiv">{{ CatalogItem.price }} руб.</p>
                    </div>
                    <p class="catalog_listen_items_product_info">подробнее</p>
                </div>
            </div>
        </div>

        <ProductModal
            ref="modal"
            @closeModal="closeModal"
            :visible="Product.visible"
            :Product="Product"
        />

    </section>
  </template>
  
  <script>
  import ProductModal from '../ModalWindows/ProductModal.vue'
  
  export default {
    name: 'Catalog',
    components: {
        ProductModal,
    },
    data() {
        return {
            Products: [
                {
                    id: 1,
                    name: 'Vip',
                    img: "/img/img-vip.9120969a.png",
                    price: '99999999',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 2,
                    name: 'Premium',
                    img: '/img/img-premium.44dda750.png',
                    price: '70',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 3,
                    name: 'Creative',
                    img: '/img/img-creative.2253e3b0.png',
                    price: '95',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 4,
                    name: 'Admin',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '120',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 5,
                    name: 'Vip',
                    img: "/img/img-vip.9120969a.png",
                    price: '35',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 6,
                    name: 'Premium',
                    img: '/img/img-premium.44dda750.png',
                    price: '70',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 7,
                    name: 'Creative',
                    img: '/img/img-creative.2253e3b0.png',
                    price: '95',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 8,
                    name: 'Admin',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '120',
                    category: 'privilegesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 9,
                    name: 'Кейс Пандоры',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '50',
                    category: 'casesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 10,
                    name: 'Титул Бамбук',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '100',
                    category: 'titlesItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 11,
                    name: 'Игровая валюта',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '90',
                    category: 'otherItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
                {
                    id: 12,
                    name: 'Мусор',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '20',
                    category: 'otherItem',
                    description: [
                        {
                            item: 'Виртуальный сундук - /ec',
                        },
                        {
                            item: 'Виртуальный верстак - /craft',
                        },
                        {
                            item: 'Узнать айди предмета - /id',
                        },
                        {
                            item: 'Зарплата - /salary',
                        },
                    ],
                    additionally: [
                        {
                            item: 'Доступен собственный набор: (/kit)',
                        },
                        {
                            item: 'Префикс привелегии: VIP',
                        },
                        {
                            item: 'Доступно аукционов: 6',
                        },
                    ],
                },
            ],
            filtersCatalog: [
                {
                    id: 'privileges',
                    name: 'Привилегии',
                },
                {
                    id: 'cases',
                    name: 'Кейсы',
                },
                {
                    id: 'titles',
                    name: 'Титулы',
                },
                {
                    id: 'other',
                    name: 'Прочее',
                },
            ],
            Product: {
                id: 1,
                name: 'ERROR',
                img: "/img/img-vip.9120969a.png",
                price: 'ERROR',
                category: 'privilegesItem',
                visible: false,
            },
        }
    },
    mounted(){
        let categoryItem = document.querySelectorAll('.catalog_listen_items')
        let privileges = document.querySelectorAll('#privilegesItem')
        let buttonPrivileges = document.getElementById('privileges')

        for(let i = 0; i < categoryItem.length; i++){
            categoryItem[i].style.display = 'none'
        }

        for(let i = 0; i < privileges.length; i++){
            privileges[i].style.display = 'block'
            privileges[i].style.opacity = 1
        }
        buttonPrivileges.classList.add('ActiveClassButton')

        if(screen.width <= 639) {
            document.getElementById('titlesItem').id = 'otherItem'
        }
    },
    methods: {
        buttonCategory(id) {
            let privileges = document.querySelectorAll('#privilegesItem')
            let cases = document.querySelectorAll('#casesItem')
            let titles = document.querySelectorAll('#titlesItem')
            let other = document.querySelectorAll('#otherItem')
            let buttonPrivileges = document.getElementById('privileges')
            let buttonCases = document.getElementById('cases')
            let buttonTitles = document.getElementById('titles')
            let buttonOther = document.getElementById('other')

            if(id === 'privileges'){
                for(let i = 0; i < privileges.length; i++){
                    setTimeout(() => {
                        privileges[i].style.display = 'block'
                    }, 85)
                    setTimeout(() => {
                       privileges[i].style.opacity = 1
                    }, 100)
                    
                }
                for(let i = 0; i < cases.length; i++){
                    cases[i].style.opacity = 0

                    setTimeout(() => {
                       cases[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < titles.length; i++){
                    titles[i].style.opacity = 0

                    setTimeout(() => {
                       titles[i].style.display = 'none'
                    }, 70)
                    
                }
                for(let i = 0; i < other.length; i++){
                    other[i].style.opacity = 0

                    setTimeout(() => {
                        other[i].style.display = 'none'
                    }, 70)    
                }
                buttonPrivileges.classList.add('ActiveClassButton')
                buttonCases.classList.remove('ActiveClassButton')
                buttonTitles.classList.remove('ActiveClassButton')
                buttonOther.classList.remove('ActiveClassButton')
            } else if(id === 'cases'){
                for(let i = 0; i < cases.length; i++){
                    setTimeout(() => {
                       cases[i].style.display = 'block'
                    }, 85)
                    setTimeout(() => {
                       cases[i].style.opacity = 1
                    }, 100)
                }
                for(let i = 0; i < privileges.length; i++){
                    privileges[i].style.opacity = 0

                    setTimeout(() => {
                        privileges[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < titles.length; i++){
                    titles[i].style.opacity = 0

                    setTimeout(() => {
                       titles[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < other.length; i++){
                    other[i].style.opacity = 0

                    setTimeout(() => {
                        other[i].style.display = 'none'
                    }, 70)    
                }
                buttonPrivileges.classList.remove('ActiveClassButton')
                buttonCases.classList.add('ActiveClassButton')
                buttonTitles.classList.remove('ActiveClassButton')
                buttonOther.classList.remove('ActiveClassButton')
            } else if(id === 'titles'){
                buttonPrivileges.classList.remove('ActiveClassButton')
                buttonCases.classList.remove('ActiveClassButton')
                buttonTitles.classList.add('ActiveClassButton')
                buttonOther.classList.remove('ActiveClassButton')
                for(let i = 0; i < titles.length; i++){
                    setTimeout(() => {
                       titles[i].style.display = 'block'
                    }, 85)
                    setTimeout(() => {
                       titles[i].style.opacity = 1
                    }, 100)
                }
                for(let i = 0; i < privileges.length; i++){
                    privileges[i].style.opacity = 0

                    setTimeout(() => {
                        privileges[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < cases.length; i++){
                    cases[i].style.opacity = 0

                    setTimeout(() => {
                        cases[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < other.length; i++){
                    other[i].style.opacity = 0

                    setTimeout(() => {
                        other[i].style.display = 'none'
                    }, 70)    
                }
            } else {
                for(let i = 0; i < other.length; i++){
                    setTimeout(() => {
                       other[i].style.display = 'block'
                    }, 85)
                    setTimeout(() => {
                       other[i].style.opacity = 1
                    }, 100)
                }
                for(let i = 0; i < privileges.length; i++){
                    privileges[i].style.opacity = 0

                    setTimeout(() => {
                        privileges[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < cases.length; i++){
                    cases[i].style.opacity = 0

                    setTimeout(() => {
                        cases[i].style.display = 'none'
                    }, 70)
                }
                for(let i = 0; i < titles.length; i++){
                    titles[i].style.opacity = 0

                    setTimeout(() => {
                        titles[i].style.display = 'none'
                    }, 70)    
                }
                buttonPrivileges.classList.remove('ActiveClassButton')
                buttonCases.classList.remove('ActiveClassButton')
                buttonTitles.classList.remove('ActiveClassButton')
                buttonOther.classList.add('ActiveClassButton')
            }
        },
        showProductModal: function (data) {
            this.Product = data
            this.Product.visible = true
            setTimeout(() => {
                document.getElementById('shadowModal').style.opacity = 1
            }, 100)
        },
        closeModal(visible) {
            document.getElementById('shadowModal').style.opacity = 0
            setTimeout(() => {
                this.Product.visible = visible
            }, 100)
        }
    }
  }
  </script>

<style lang="sass" scoped>
    .ActiveClassButton
        border-bottom: 11px solid !important
        border-image-source: linear-gradient(90deg, #FFDD00, #FBB034) !important
        border-image-slice: 1 !important
        transition: 0 !important
    .adaptiv
        display: none !important
    .catalog
        background-color: #F3F3F3
        padding-bottom: 80px
        min-height: calc(100vh - 185px)
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
            max-width: 1200px
            display: flex
            flex-wrap: wrap
            margin: auto
            margin-top: 80px
            justify-content: center

            &_items
                max-width: 1200px
                display: flex
                opacity: 0
                transition: 0.2s
                cursor: pointer
                margin: 15px
                &_product
                    background: #fff
                    width: 270px
                    height: 270px
                    display: flex
                    align-items: center
                    flex-direction: column
                    &_name
                        font-size: 24px
                        font-family: 'Montserrat-bold'
                        margin-top: 20px
                        text-align: center
                        text-transform: uppercase
                    &_image
                        display: block
                        margin-top: 17px
                    &_price
                        font-size: 16px
                        text-align: center
                        margin-top: 17px
                        border-radius: 5px
                        font-family: 'Montserrat-bold'
                        background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
                        padding: 5px 10px
                        min-width: 98px
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
                
@media (max-width: 639px)
    #titles
        display: none
    .no-adaptiv
        display: none
    .adaptiv
        display: block !important
    .catalog
        background: #D9D9D9
        &_block
            &_nav
                button
                    margin-right: 20px
                    margin-left: 20px
        &_listen
            &_items
                width: 100%
                margin-top: 12.5px
                margin-bottom: 12.5px
                height: 115px
                &_product
                    width: auto
                    height: 115px
                    display: flex
                    flex-direction: row
                    border-radius: 9px
                    padding-left: 10px
                    padding-right: 10px
                    &_image
                        width: 124px
                        height: 95px
                        margin-top: 0px
                    &_info
                        display: block
                        margin-left: auto
                        margin-right: 20px
                    &_name
                        margin-top: 0px
                        text-align: left
                    &_price
                        margin-top: 5px
                        min-width: 68px
                        border-radius: 0px
                    div
                        margin-left: 10px
                        display: flex
                        flex-direction: column
                        align-items: flex-start
@media (max-width: 468px)
    .catalog
        &_listen
            padding-left: 10px
            padding-right: 10px
            &_items
                margin-left: 0px
                margin-right: 0px
                &_product
                    &_info
                        font-weight: 400
                        font-size: 10px
                        line-height: 12px
                        margin-right: 5px
                    &_name
                        font-weight: 700
                        font-size: 17px
                        line-height: 21px
                    &_price
                        font-weight: 500
                        font-size: 13px
                        line-height: 16px
                    div
                        margin-left: 0px
</style>

