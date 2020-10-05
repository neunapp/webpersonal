<template>
  <div class="personal-data">
    <div class="personal-data__left">
      <div class="personal-data__left__content">
        <span class="personal-data__left__content__text">Hola</span>
        <h3 class="personal-data__left__content__name">Soy Luffy</h3>
        <p class="personal-data__left__content__description">
          Soy un pirata capitan de un barco y tengo el curpo de goma, por haber comido una fruta del diablo
        </p>
        <v-button-main 
          texto="Contactar"
          :color-texto="color2"
          :color-fondo="color1"
        />
      </div>
    </div>
    <div class="personal-data__right">
      <img 
        class="personal-data__right__img"
        src="../../assets/luffy.png">
    </div>
  </div>
  <the-contac />
</template>

<script>

  import VButtonMain from '@/components/base/VButtonMain'

  import { colorone, colortwo } from '@/components/_app.scss'

  import TheContac from '@/components/home/TheContac'

  export default {
    name: 'ThePersonalData',
    data() {
      return {
        color1: colorone,
        color2: colortwo
      }
    },
    components: {
      VButtonMain,
      TheContac
    }
  }
</script>

<style lang="scss" scoped>

@import '../_app.scss';

.personal-data {
  display: flex;
  &__left {
    background: $color1;
    width: 60%;
    display: flex;
    justify-content: center;
    align-items: center;
    &__content {
      width: 300px;
      color: $color-white;
      &__text {
        font-family: $ff-secondary;
        font-size: 14px;
        margin-bottom: 10px;
      }
      &__name {
        font-family: $ff-primary;
        font-size: 24px;
        color: $color2;
        margin-bottom: 10px;
      }
      &__description {
        font-family: $ff-secondary;
        font-size: 15px;
        margin-bottom: 2em;
      }
    }
  }
  &__right {
    background: $color2;
    width: 40%;
    &__img {
      width: 200px;
      position: relative;
      left: -100px;
    }
  }
}



</style>