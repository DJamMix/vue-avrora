<template>
    <section class="catalog">
        <div class="catalog_catalog-block">
            <div class="catalog_catalog-block_nav">
                <button>Привилегии</button>
                <button>Кейсы</button>
                <button>Титулы</button>
                <button>Прочее</button>
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
        padding-bottom: 166px
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
                    margin-left: 30px
                    margin-right: 30px
                button:hover
                    border-bottom: 11px solid 
                    border-image-source: linear-gradient(90deg, #FFDD00, #FBB034)
                    border-image-slice: 1
                    transition: 0.2s
</style>

