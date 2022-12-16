<template>
    <section class="rules">
        <div class="rules_rules-block">
            <div class="rules_rules-block_text">
                <h2>ПРАВИЛА ПРОЕКТА</h2>
                <div></div>
            </div>
            <List />
        </div>
    </section>
</template>

<script>
  import List from '../Main/List.vue'

export default {
  components: {
    List
  }
}
</script>

<style lang="sass" scoped>
        .rules
            padding-top: 63px
            padding-bottom: 67px
            background: #F3F3F3
            &_rules-block
                max-width: 1170px
                margin: auto 
                &_text
                    position: relative
                    padding-bottom: 62px
                    h2
                        font-size: 27px
                        font-family: 'Montserrat-extrabold'
                        font-weight: 800
                        text-align: center
                    div
                        background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
                        width: 58px
                        height: 16px
                        margin-left: 680px
                        margin-top: -33px

                
</style>