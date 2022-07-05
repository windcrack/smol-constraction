<template lang="pug">
    .reviews-page-body
        h2.title.title_bottom48 Оставить отзыв
        form.form(@submit.prevent="send")
            label(for="nameForm").label.label_bottom14 Ваше имя
            input(type="text" v-model="name" placeholder="Введите своё имя" required).input#nameForm.
            span.error-input(v-if="!$v.name.minLength") Имя дожно быть не менее {{ $v.name.$params.minLength.min }}х символов.
            label(for="email").label.label_bottom14 Ваш адрес электронной почты
            input(type="email" v-model="email" placeholder="Введите свой e-mail" required).input#email
            span.error-input(v-if="!$v.email.email") Введите пожалуйста почту в формате xxxxx@xxx.xx
            label(for="text" required).label.label_bottom14 Отзыв
            textarea(placeholder="Введите свой e-mail").input.input_text#text
            recaptcha
            p.policity Нажимая кнопку «Заказать звонок» вы соглашаетесь с правилами 
                nuxt-link(to="/privacypolicy").underlined-text Пользовательского соглашения
            button.button.button_radius30.button_color.button_padding.button_border-green
                span.button__text отправить
        img(src="/img/greenblock2.png").green-block.green-block_form-one
        img(src="/img/greenblock2.png").green-block.green-block_form-two
        //- SendReview
</template>

<script>
import { minLength, email } from "vuelidate/lib/validators";

    export default {
        data(){
            return{
                name: '',
                email: '',
            }
        },

        validations: {
            name: {
                minLength: minLength(4),
            },
            email: {
                email,
                minLength: minLength(6),
            }
        },

        methods: {
            send() {
                this.$v.$touch();
                if (this.$v.$invalid) {
                    alert("Имя должно быть не мении 4 символов");
                } else {
                    console.log(this.name);
                    console.log(this.email);
                }
            },
        },
    }
</script>

<style lang="scss">
    .reviews-page-body{
        margin: 58px auto 79px;
        position: relative;
    }
</style>