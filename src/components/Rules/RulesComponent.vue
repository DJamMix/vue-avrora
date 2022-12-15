<template>
    <section class="rules">
        <div class="rules_rules-block">
            <div class="rules_rules-block_text">
                <h2>ПРАВИЛА ПРОЕКТА</h2>
                <div></div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'RulesComponent',
    components: {

    }
}
</script>

<style lang="sass" scoped>
        .rules
            padding-top: 63px
            padding-bottom: 267px
            background: #F3F3F3
            &_rules-block
                max-width: 1170px
                margin: auto 
                &_text
                    position: relative
                    h2
                        font-size: 25px
                        font-family: 'Montserrat-extrabold'
                        font-weight: 800
                        text-align: center
                    div
                        background: linear-gradient(309deg, rgba(251,176,52,1) 0%, rgba(255,221,0,1) 100%)
                        width: 58px
                        height: 16px
                        margin-left: 680px
                        margin-top: -30px

                
</style>