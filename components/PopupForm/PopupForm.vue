<template lang="pug">
.popup-question
  h3.title Остались вопросы?
  form.popup-form(@submit.prevent="send")
    label.label.label_bottom14(for="name") Ваше имя
    input#naem.input(type="text" placeholder="Введите своё имя" v-model="name")
    span.error-input(v-if="!$v.name.minLength") Имя дожно быть не менее {{ $v.name.$params.minLength.min }}х символов.
    label.label.label_bottom14(for="phone") Ваш номер телефона
    input#phone.input(
      type="text",
      v-imask="mask",
      placeholder="+7 (___) ___-__-__"
    )
    recaptcha
    p.policity Нажимая кнопку «Заказать звонок» вы соглашаетесь с правилами Пользовательского соглашения
    button.button.button_color.button_radius30.button_border-green.button_padding
      span.button__text Заказать звонок
</template>

<script>
import { minLength } from "vuelidate/lib/validators";
import { IMaskDirective } from "vue-imask";
export default {
  data() {
    return {
      mask: {
        mask: "+7 000 000-00-00",
        lazy: true,
      },
      name: "",
    };
  },
  validations: {
    name: {
      minLength: minLength(4),
    },
  },
  directives: {
    imask: IMaskDirective,
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
};
</script>

<style lang="scss">
.popup-question {
  
}

.popup-form {
  display: flex;
  flex-direction: column;
}
</style>
