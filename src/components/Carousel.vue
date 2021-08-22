<template>
  <div class="carousel">
    <button class="btn arrow"><i class="fas fa-arrow-left"></i></button>
      <Card
      v-for="carousel in videos" :key="carousel.id"
      :title="carousel.title"
      :daytime="carousel.daytime"
      :description="carousel.description"
      :src="carousel.src"
      :tag="carousel.tag"
      :class_description="carousel.class_description"
      :class_title="carousel.class_title"/>
     <button class="btn arrow"><i class="fas fa-arrow-right"></i></button>
  </div>
</template>

<script>
import Card from './Card.vue'

  export default {
    components: {
      Card,
    },
    data() {
      return {
        videos: [
          {
            title: "Défense d’afficher – La ville de Paris contre l’affichage sauvage",
            daytime: "10 août 2021",
            src: require("@/assets/images/video3.png"),
          },
           {
            title: "Réforme législative du droit d’accès aux archives « secret-défense » : l’apport de la loi « PTAR » du 30 juillet 2021",
            daytime: "10 août 2021",
            src: require("@/assets/images/video4.png"),
          },
           {
            title: "La loi Egalim n’a pas résolu les relations entre les agriculteurs et la grande distribution",
            daytime: "10 août 2021",
            src: require("@/assets/images/video5.png"),
          }
        ]
      }
    },
  }
</script>

<style lang="stylus">
.carousel
  display flex
  .card:nth-child(even)
    display none
  .card 
    width 350px
    .card__title
      font-size 25px
  .card img
    width 100%
  
  .btn.arrow
    padding: 21px 16px 21px 17px;
    background-color: #ffb563;
    color #2d2d2d
    border none
    margin auto 0

  .card:hover
    .card__title 
      text-decoration underline

@media (min-width: 1131px)
  .carousel
    flex-direction row
    justify-content space-around
    .card
      display block !important


</style>