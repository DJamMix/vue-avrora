<template>
    <section class="catalog">
        <div class="catalog_block">
            <div class="catalog_block_nav">
                <button @click="buttonCategory(filterCatalog.id)" class="catalog_block_nav_btn button-category" v-for="filterCatalog in filtersCatalog" :key="filterCatalog.id" :id="filterCatalog.id">{{ filterCatalog.name }}</button>
            </div>
        </div>
        <div class="catalog_listen">
            <div class="catalog_listen_items" :id="CatalogItem.category" v-for="CatalogItem in Catalog" :key="CatalogItem.id">
                <div class="catalog_listen_items_product">
                    <p class="catalog_listen_items_product_name">{{ CatalogItem.name }}</p>
                    <img class="catalog_listen_items_product_image" :src="CatalogItem.img" alt="Товар">
                    <p class="catalog_listen_items_product_price">{{ CatalogItem.price }} руб.</p>
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

    },
    data() {
        return {
            Catalog: [
                {
                    id: 1,
                    name: 'Vip',
                    img: "/img/img-vip.9120969a.png",
                    price: '35',
                    category: 'privilegesItem',
                },
                {
                    id: 2,
                    name: 'Premium',
                    img: '/img/img-premium.44dda750.png',
                    price: '70',
                    category: 'privilegesItem',
                },
                {
                    id: 3,
                    name: 'Creative',
                    img: '/img/img-creative.2253e3b0.png',
                    price: '95',
                    category: 'privilegesItem',
                },
                {
                    id: 4,
                    name: 'Admin',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '120',
                    category: 'privilegesItem',
                },
                {
                    id: 5,
                    name: 'Vip',
                    img: "/img/img-vip.9120969a.png",
                    price: '35',
                    category: 'privilegesItem',
                },
                {
                    id: 6,
                    name: 'Premium',
                    img: '/img/img-premium.44dda750.png',
                    price: '70',
                    category: 'privilegesItem',
                },
                {
                    id: 7,
                    name: 'Creative',
                    img: '/img/img-creative.2253e3b0.png',
                    price: '95',
                    category: 'privilegesItem',
                },
                {
                    id: 8,
                    name: 'Admin',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '120',
                    category: 'privilegesItem',
                },
                {
                    id: 9,
                    name: 'Кейс Пандоры',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '50',
                    category: 'casesItem',
                },
                {
                    id: 10,
                    name: 'Титул Бамбук',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '100',
                    category: 'titlesItem',
                },
                {
                    id: 11,
                    name: 'Игровая валюта',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '90',
                    category: 'otherItem',
                },
                {
                    id: 12,
                    name: 'Мусор',
                    img: '/img/img-admin.c3d65d0e.png',
                    price: '20',
                    category: 'otherItem',
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
            max-width: 1170px
            display: flex
            flex-wrap: wrap
            margin: 0 auto
            &_items
                margin: 0 auto
                margin-top: 40px
                max-width: 1170px
                display: flex
                opacity: 0
                transition: 0.2s
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
                        text-transform: uppercase
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

