<template lang="pug">
    form.vacancy-form(@submit.prevent="send")
        label(for="name").label.label_bottom14 Ваше имя и фамилия
        input(type="text" v-model="name" placeholder="Введите своё имя и фамилию" required).input#name
        span.error-input(v-if="!$v.name.minLength") Имя дожно быть не менее {{ $v.name.$params.minLength.min }}х символов.
        label(for="email").label.label_bottom14 Ваш адрес электронной почты
        input(type="email" v-model="email" placeholder="Введите свой e-mail" required).input#email
        span.error-input(v-if="!$v.email.email") Введите пожалуйста почту в формате xxxxx@xxx.xx
        label(for="moretext").label.label_bottom14 Ваше предыдущее место работы и должность
        textarea(placeholder="Введите информацию ..." required).input.input_text#moretext
        label(for="file").label__file Загрузить резюме..
            span.label__file-sub (не обязательно)(файл не более 2 МБ, в формате doc или pdf)
        input#file(type="file")
        recaptcha
        p.policity Нажимая кнопку «Заказать звонок» вы соглашаетесь с правилами 
            nuxt-link(to="/privacypolicy").underlined-text Пользовательского соглашения
        button.button.button_color.button_radius30.button_border-green.button_padding
            span.button__text отправить
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
                }
            },
        },
    }
</script>

<style lang="scss">
    .vacancy-form{
        display: flex;
        flex-direction: column;

        &__text{
            height: 140px;
            resize: none;
            margin-bottom: 15px;
        }


        #file{
            display: none;
        }
    }
</style>