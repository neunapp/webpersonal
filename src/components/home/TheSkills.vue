<template>
  <div class="skills">
    <h3 class="skills__title">Mis Habilidades</h3>
    <p class="skills__text">
      Después de consumir la fruta Gomu Gomu, el cuerpo de Luffy se convirtió como el caucho, dándole la capacidad de estirar distancias.
    </p>
    <div class="skills__items">
      <div 
        class="skills__item"
        v-for="habilidad in habilidades"
        :key="habilidad.id">
          <v-card-main
            :titulo="habilidad.titulo"
            :contenido="habilidad.contenido"
            :color="habilidad.color"
           />
      </div>
    </div>
  </div>
</template>

<script>

  import { colortwo, colorthree,colorfour, colorfive } from '@/components/_app.scss'
  import VCardMain from '@/components/base/VCardMain'

  export default {
    name: 'TheSkills',
    data() {
      return {
        habilidades: [
          {'id': 0, titulo: 'Gomu Gomu', contenido: 'Después de consumir la fruta Gomu Gomu, el cuerpo de Luffy se convirtió como el caucho', color: colortwo},
          {'id': 1, titulo: 'Fuerza', contenido: 'fuerza física, con la que es capaz de destrozar incluso piedras o acero con sus propias manos', color: colorthree},
          {'id': 2, titulo: 'Haoshoku haki', contenido: 'Pposee haoshoku haki un tipo de Haki de alto nivel con el que sólo una de cada un millón de personas nacen', color: colorfour},
          {'id': 3, titulo: 'resistencia', contenido: 'Programador en Vue 2 con 3 años de experiencia, trabaje en PyImage, PyGames', color: colorfive},
        ]
      }
    },
    components: {
      VCardMain
    }
  }
</script>

<style lang="scss" scoped>

  @import '../_app.scss';

  .skills {
    background: $color1;
    padding: 4em;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    &__title {
      font-family: $ff-primary;
      color: $color-white;
      margin-bottom: 1em;
      font-size: 24px;
    }
    &__text {
      font-family: $ff-secondary;
      color: $color-white;
      margin-bottom: 1em;
    }
    &__items {
      display: grid;
      grid-template-columns: 400px 400px;
    }
  }
</style>