<template>
  <div class="block-1 py-4">
    <Header/>

    <div class="container">
      <div class="row">
        <div class="col-lg-5">
          <h1 class="mb-3">
            Отчет о продвижении сайта
            <a :href="siteUrl" traget="_blank">{{ siteUrlWithoutProtocol }}</a>
          </h1>

          <span class="font-weight-500">(ООО Тест)</span>

          <div class="row mt-4">
            <div class="col-6">
              <Select :options="month"/>
            </div>
            <div class="col-6">
              <Select :options="month"  class="select--transparent" />
            </div>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="col-lg-3">
          <InfoBlock
            name="посетителей"
            value="503 000"
            text="Это на 13% выше, чем в этот же период в прошлом году (437 610 посетителей)"
            hint="Всплывающий текст"
            arrow="up"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Select from '@/components/Select.vue';
import InfoBlock from '@/components/InfoBlock.vue';

export default {
  name: 'Block1',
  components: {
    Header,
    Select,
    InfoBlock,
  },
  data() {
    return {
      siteUrl: 'https://test.ru',
      month: [
        {
          name: 'Январь',
          value: 1,
        },
        {
          name: 'Февраль',
          value: 2,
        },
        {
          name: 'Март',
          value: 3,
        },
        {
          name: 'Апрель',
          value: 4,
        },
        {
          name: 'Май',
          value: 5,
        },
        {
          name: 'Июнь',
          value: 6,
        },
        {
          name: 'Июль',
          value: 7,
        },
        {
          name: 'Август',
          value: 8,
        },
        {
          name: 'Сентябрь',
          value: 9,
        },
        {
          name: 'Октябрь',
          value: 10,
        },
        {
          name: 'Ноябрь',
          value: 11,
        },
        {
          name: 'Декабрь',
          value: 12,
        },
      ],
    };
  },
  computed: {
    siteUrlWithoutProtocol() {
      const url = this.siteUrl;
      let lengthProtocol = 0;

      if (url.indexOf('https://') !== false) {
        lengthProtocol = 8;
      } else if (url.indexOf('http://') !== false) {
        lengthProtocol = 7;
      }

      return url.substr(lengthProtocol);
    },
  },
};
</script>

<style lang="scss" scoped>
  .block-1 {
    position: relative;
    min-height: 100vh;
    background-image: url(../../assets/img/bg-block-1.jpg);
    background-position: top center;
    background-size: cover;

    &:after {
      content: '';
        position: absolute;
        bottom: 0;
        right: 0;
        border-top: 5.26rem solid transparent;
        border-right: 100vw solid #ffff;
        padding-bottom: 0.5rem;
    }
  }
</style>
