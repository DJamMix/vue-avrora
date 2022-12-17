<template>
    <div class="faq" id="faq">
        <div class="faq_questions-answers" v-for="questionAnswer in questionsAnswers" :key="questionAnswer.id">
            <p class="faq_questions-answers_question">{{ questionAnswer.question }}</p>
            <div class="faq_questions-answers_answer" v-for="Answers in Answers" :key="Answers.id">
               {{ Answers.Answer }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AuthView',
    components: {

    },
    data() {
        return {
            questionsAnswers: [
                {
                    id: 1,
                    question: 'Где будут располагаться курсы?',

                },
            ],
            Answers: [
                {
                    id:1,
                    Answer: [
                        '123123',
                        '123123123123'
                    ]
                }
            ]
        }
    },
    mounted() {
        let accordion = document.getElementsByClassName('faq_questions-answers_question');

                const element = document.getElementsByClassName('faq')[0];
            setTimeout(() => {
                element.style.setProperty('--height', element.offsetHeight + 'px')
            }, 500)
        for (let i = 0; i < accordion.length; i++) {
            accordion[i].addEventListener('click', () => {
                let panel = accordion[i].parentElement.children[1];
                element.style.setProperty('--height', element.offsetHeight+100 + 'px')
                
                if (panel.style.maxHeight) {

                    panel.style.maxHeight = null

                } else {

                    panel.style.maxHeight = panel.scrollHeight + 'px';

                }
            })
            
        }

        window.addEventListener('resize', () => {
            element.style.setProperty('--height', element.offsetHeight+100 + 'px')
        })
    }
}
</script>

<style lang="sass" scoped>
    .faq
        &_questions-answers
            position: relative
            // margin-bottom: 33px
            &::after
                content: ''
                width: 100%
                height: 1px
                // top: 39px
                top: 45px
                border-radius: 8px
                background: rgba(57, 57, 57, 0.8)
                position: absolute
            &_question
                font-size: 23px
                margin-bottom: 33px
                cursor: pointer
                // transition: 0.4s
            &_answer
                color: #393939
                overflow: hidden
                max-height: 0
                transition: max-height 0.2s ease-out
                margin-bottom: 40px
                max-width: 630px
</style>