<template>
  <div class="about">
    <div class="about__content">
      <div class="about__content__left">
        <img 
          class="about__content__left__img"
          src="../../assets/luffy2.jpeg">
      </div>
      <div class="about__content__right">
        <h3 class="about__content__right__title">Sobre Mi</h3>
        <p class="about__content__right__text">
           Monkey D. Luffy es el protagonista principal del anime y manga One Piece. Su cuerpo está hecho de goma después de comerse una fruta del diablo,
        </p>
        <div class="about__content__right__ctrls">
          <v-button-main 
            texto="Linkeding"
            :color-texto="color2"
            :color-fondo="color1"
          />
          <v-button-main 
            texto="Github"
            :color-texto="color1"
            :color-fondo="color2"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  import VButtonMain from '@/components/base/VButtonMain'

  import { colorone, colortwo } from '@/components/_app.scss'

  export default {
    name: 'TheAbout',
    data() {
      return {
        color1: colorone,
        color2: colortwo
      }
    },
    components: {
      VButtonMain
    }
  }
</script>

<style lang="scss" scoped>

  @import '../_app.scss';

  .about {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 5em;
    padding-bottom: 5em;
    background: $color1;
    opacity: 0.95;
    &__content {
      width: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      &__left {
        border: 1px solid $color2;
        width: 150px;
        height: 200px;
        margin-right: 3em;
        &__img {
          width: 100%;
          height: 100%;
          position: relative;
          left: 20px;
          top: -20px;
        }
      }
      &__right {
        display: block;
        width: 50%;
        color: $color-white;
        &__title {
          font-family: $ff-primary;
          font-size: 20px;
          border-bottom: 1px solid $color2;
          margin-bottom: 1em;
          padding-bottom: 1em;
        }
        &__text {
          font-size: 15px;
          font-family: $ff-secondary;
          margin-bottom: 1.5em;
        }
      }
    }
  }
</style>