<template>
  <div class="carousel">
    <a class="btn arrow"><i class="fas fa-arrow-left"></i></a>
      <Card
      v-for="carousel in videos" :key="carousel.id"
      :title="carousel.title"
      :daytime="carousel.daytime"
      :description="carousel.description"
      :src="carousel.src"
      :tag="carousel.tag"
      :class_description="carousel.class_description"
      :class_title="carousel.class_title"/>
     <a class="btn arrow"><i class="fas fa-arrow-right"></i></a>
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
            src: require("@/assets/images/article-cover.png"),
          },
           {
            title: "Réforme législative du droit d’accès aux archives",
            daytime: "10 août 2021",
            src: require("@/assets/images/article-cover.png"),
          },
           {
            title: "La loi Egalim n’a pas résolu les relations entre ",
            daytime: "10 août 2021",
            src: require("@/assets/images/article-cover.png"),
          }
        ]
      }
    },
  }
</script>

<style lang="stylus">
.carousel
  display flex
  justify-content space-around
  align-items center
  .card 
    width 350px
  .card img
    width 350px !important
  .btn.arrow
    padding: 21px 16px 21px 17px;
    background-color: #ffb563;
    color #2d2d2d
</style>