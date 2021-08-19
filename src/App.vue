<template>
  <div id="app">
    <!-- <img src="./assets/img-conseil-constitutionnel.png" alt=""> -->
    <div class="container">
      <section class="article-cover">
        <Card 
            v-for="article in covers" :key="article.id"
            :title="article.title"
            :daytime="article.daytime"
            :description="article.description"
            :src="article.src"
            :tag="article.tag"
          />
      </section>
      <section>
        <div class="flex">
          <Card 
            v-for="article in articles" :key="article.id"
            :title="article.title"
            :daytime="article.daytime"
            :description="article.description"
            :src="article.src"
            :tag="article.tag"
            :alt="article.alt"
          />
        </div>
      </section>
      <section class="">
        <h2>Nos présidents d’honneur</h2>
       <div class="presentation__members">
          <Card 
          v-for="member in members" :key="member.id"
          :title="member.title"
          :daytime="member.daytime"
          :description="member.description"
          :src="member.src"
          :tag="member.tag"
          :alt="member.alt"
        />
       </div>
      </section>
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  data() {
    return {
      covers: [
        {
          title: "L’Union européenne se lance dans la course au standard des obligations vertes, par Sylvie Schmitt",
          description: "Le 6 juillet 2021, la Commission européenne a rendu publique sa stratégie de promotion de la finance durable. Deux projets de textes ont été présentés à cette occasion. Le premier …",
          daytime: "10 août 2021",
          src: "/img/article-cover.ac440c71.png",
          tag: "L’actualité au prisme du droit"
        }
      ],
      articles: [
        {
          title: "L’Union européenne se lance dans la course au standard des obligations vertes, par Sylvie Schmitt",
          description: "Le vote de la loi sous la Ve République est un exercice juridique convenu dont les acteurs sont identifiés et la conclusion souvent connue à l’avance.",
          daytime: "10 août 2021",
          src: "/img/img-conseil-constitutionnel.f510128a.png",
          tag: "L’actualité au prisme du droit"
        },
        {
          title: "Le Tribunal constitutionnel espagnol censure l’état d’alarme : Vice juridique ou erreur politique ?",
          description: "L’information a filtré et elle a fait l’effet d’une bombe : le 14 juillet dernier, l’assemblée plénière du Tribunal constitutionnel espagnol a partiellement fait droit au recours d’inconstitutionnalité formé par le parti politique",
          daytime: "10 août 2021",
          src: "/img/img-spanish-flag.b9f4ca69.png",
          tag: "L’actualité au prisme du droit"
        }
      ],
      members: [
        {
          title: "Elisabeth Baraduc",
          description: "Avocat au Conseil d’Etat et à la Cour de cassation - Baraduc&Duhamel",
          src: "/img/elisabeth_baraduc.2521ee52.png",
          alt: "Portrait d'Elisabeth Baraduc"
        },
        {
          title: "Christine Lagarde",
          description: "Présidente de la Banque centrale européenne (BCE)",
          src: "/img/christine_lagarde.538bc368.png",
          alt: "Portrait de Christine Lagarde"
        },
        {
          title: "Alexandre de Juniac",
          description: "Directeur Général de l’Association Internationale du Transport Aérien",
          src: "/img/alexandre_de_juniac.fc2ceda0.png",
          alt: "Portrait d'Alexandre de Juniac",
          class: "bw-hover"
        }
      ]
    }
  },
}
</script>

<style lang="stylus">
#app 
  font-family: 'Poppins', sans-serif;

.container {
  width 80%
  margin 0 auto
}
.article-cover
  .card 
    width 100%
    img
      max-width 100%
.flex 
  display flex
  justify-content space-between
  .card 
    width 526px
    img
      max-width 100%
.presentation__members 
  display flex
  justify-content space-around
  .card 
    width 350px
    img
      max-width 100%
      filter grayscale(1)
  .card:hover
    .card__title
      text-decoration  underline
    img:hover
      filter grayscale(0)

</style>
