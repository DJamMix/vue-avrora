<template>
    <section class="rules">
        <div class="rules_rules-block">
            <div class="rules_rules-block_object">
                <h2>ПРАВИЛА ПРОЕКТА<div></div></h2>
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
                margin: auto 
                max-width: 1170px
                &_object
                    padding-bottom: 62px
                    position: relative
                    justify-content: center
                    align-items: center
                    text-align: center
                    h2
                        font-size: 27px
                        font-family: 'Montserrat-extrabold'
                        font-weight: 800
                        text-align: center
                        div
                            background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
                            width: 58px
                            margin-left: 59%
                            margin-top: -3%
                            height: 16px
</style>