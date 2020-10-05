<template>
  <div class="contacto">
    <div class="contacto__content">
      <p class="contacto__content__text">Email: neunapp.cursos@gmail.com</p>
      <p class="contacto__content__text">Telegram: @cscthian</p>
      <a href="#" class="contacto__content__btn">Cerrar</a>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TheContac'
  }
</script>

<style lang="scss" scoped>

  @import '../_app.scss';

  .contacto {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    width: 100%;
    height: 100vh;
    top: 0px;
    left: 0px;
    z-index: 100;
    background: rgba(146, 141, 141, 0.5);
    &__content {
      width: 300px;
      background: $color2;
      padding: 1em;
      border-radius: 10px;
      &__btn {
        display: block;
        text-align: center;
        font-family: $ff-primary;
      }
    }
  }
</style>