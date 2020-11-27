<template>
  <header class="header">
    <div class="container">
      <div class="row align-items-center">
        <div class="col">
          <Logo :src="logo"/>
        </div>

        <div class="col-auto">
          Ваш менеджер: {{ managerName }}
        </div>

        <div class="col-auto">
          <PhoneLink :phone="phone"/>
        </div>

        <div class="col-auto">
          <Btn :name="btnName"/>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import logoSrc from '@/assets/img/logo.svg';
import PhoneLink from '@/components/PhoneLink.vue';
import Btn from '@/components/Btn.vue';
import Logo from '@/components/Logo.vue';

export default {
  name: 'Header',
  components: {
    PhoneLink,
    Btn,
    Logo,
  },
  data() {
    return {
      managerName: 'Сергей',
      phone: '8 (927) 432-54-54',
      btnName: 'Заказать звонок',
      logo: logoSrc,
    };
  },
};
</script>

<style lang="scss" scoped>
  .header {
    font-weight: 500;
    font-size: 13px;
    line-height: 16px;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: #333333;
  }
</style>
