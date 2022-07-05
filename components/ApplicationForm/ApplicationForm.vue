<template lang="pug">
    form.application-form(@submit.prevent="send")
        label(for="name").label.label_bottom14 Ваше имя
        input(type="text" v-model="name" placeholder="Введите своё имя" required).input#name
        span.error-input(v-if="!$v.name.minLength") Имя дожно быть не менее {{ $v.name.$params.minLength.min }}х символов.
        label(for="phone").label.label_bottom14 Ваш номер телефона
        input(type="phone" v-imask="mask"  placeholder="+7 (___) ___-__-__" required).input#phone
        recaptcha
        p.policity Нажимая кнопку «Заказать звонок» вы соглашаетесь с правилами 
            nuxt-link(to="/privacypolicy").underlined-text Пользовательского соглашения
        button.button.button_radius30.button_color.button_padding.button_border-green
            span.button__text Заказать звонок
</template>

<script>
import { IMaskDirective } from 'vue-imask';
import { minLength } from 'vuelidate/lib/validators'
    export default {

        data(){
            return{
                mask:{
                    mask: '+7 000 000-00-00',
                    lazy: true,
                },
                name: '',
            }
        },

        methods:{
            send() {
                this.$v.$touch();
                if (this.$v.$invalid) {
                    alert("Имя должно быть не мении 4 символов");
                } else {
                    console.log(this.name);
                }
            },
        },

        validations:{
            name:{
                minLength: minLength(4),
            },
        },

        directives: {
            imask: IMaskDirective
        },
    }
</script>

<style lang="scss">
    .application-form{
        display: flex;
        flex-direction: column;
        width: 484px;

        @media screen and (max-width: 600px){
            width: 283px;
        }
    }
</style>