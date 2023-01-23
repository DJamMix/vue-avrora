<template>
    <div class="faq" id="faq">
        <div class="faq_questions-answers" v-for="questionAnswer in questionsAnswers" :key="questionAnswer.id">
            <p class="faq_questions-answers_question">{{ questionAnswer.question }}</p>
            <div class="faq_questions-answers_answer">{{ questionAnswer.answer }}</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'List',
    components: {

    },
    data() {
        return {
            questionsAnswers: [
                {
                    id: 1,
                    question: 'Основные правила проекта',
                    answer: [
                        {
                            point: '1.1 Незнание правил не освобождает вас от ответственности.'
                        },
                        {
                            point: '1.2 Начав играть на наших серверах, Вы автоматически подтверждаете своё согласие с данным сводом правил.'
                        },
                        {
                            point: '1.3 Администрация вправе наказать игрока по причине, не указанной в настоящих правилах.'
                        },
                        {
                            point: '1.4 Администрация не несет ответственности за временную или постоянную невозможность игры на сервере конкретным лицом или группой лиц.'
                        },
                        {
                            point: '1.5 Администрация имеет право корректировать данный свод правил без уведомления игрока.'
                        }
                    ]
                },
                {
                    id: 2,
                    question: 'Правила игроков с привилегией',
                    answer: [
                        {
                            point: '2.1 Ложный кик / Ложный мут / Ложный бан - Бан от 6 часов до 3 дней'
                        },
                        {
                            point: '2.2 Некорректная причина мута/кика/бана - Бан от 6 часов до 1 дня.'
                        },
                        {
                            point: '2.3 Мат / Оскорбление в причине мута/кика/бана - Бан на 12 часов'
                        },
                        {
                            point: '2.4 Превышение срока наказания - Бан от 3 часов до 2 дней'
                        },
                        {
                            point: '2.5 Размут нарушителя без причины - Бан от 1 часа до 1 дня'
                        },
                        {
                            point: '2.6 Выдача наказания без доказательств - Бан от 12 часов до 2 дней'
                        },
                        {
                            point: '2.7 Флуд командой /afk - Бан от 30 минут до 3 часов'
                        }
                    ]
                },
                {
                    id: 3,
                    question: 'Защита и безопасность аккаунта',
                    answer: [
                        {
                            point: '3.1 Игрок полностью отвечает за надёжность своего пароля и доступа к аккаунту. Не забывайте о привязке к ВК!'
                        },
                        {
                            point: '3.2 Запрещено передавать, продавать, обменивать, разыгрывать аккаунт кому-либо. Предусматривается наказание: Перманентная блокировка аккаунта.'
                        },
                        {
                            point: '3.3 Подделывание никнейма на схожий с никнеймом другого игрока, с целью навредить или подставить. Предусматривается наказание: Перманентная блокировка всех аккаунтов нарушителя.'
                        },
                        {
                            point: '3.4 Ник не должен содержать мата, оскорблений и тд быть схожим с ником администрации/модератора. Предусматривается наказание: Перманентная блокировка аккаунта.'
                        },
                        {
                            point: '3.5 Ответственность несёт владелец аккаунта, независимо от того, кто совершал действия под данным аккаунтом.'
                        }
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
            margin-top: 32px
            display: flex
            justify-content: center
            align-items: center
            flex-direction: column
            align-content: center
            text-transform: uppercase
            &_question
                font-size: 16px
                display: flex
                justify-content: center
                align-items: center
                text-align: center
                background: #fff
                border-radius: 10px
                width: 682px
                height: 56px   
                font-family: 'Montserrat-bold'
                cursor: pointer
            &_answer
                font-family: 'Montserrat-medium'
                font-size: 13px
                justify-content: center
                align-items: center
                text-align: center
                background: #fff
                border-radius: 10px
                margin-top: 33px
                width: 682px
                overflow: hidden
                max-height: 0
                transition: max-height 0.2s ease-out
//Адаптив

@media (max-width: 850px)
    .faq
        &_questions-answers
            &_question
                width: 75%
            &_answer
                width: 75%

</style>