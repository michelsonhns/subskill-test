<template>
  <div id="app">
    <Navbar/>
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
    </div>
    <section class="members-container">
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
        <button>Découvrir les membres du club</button>

    </section>

    <section class="news-container">
      <div class="">
        <h2>La semaine juridique</h2>
        <div class="card-group">
          <CardHorizontal
          v-for="newsletter in news" :key="newsletter.id"
          :title="newsletter.title"
          :description="newsletter.description"
          :direction="newsletter.direction"
          :src="newsletter.src"/>
        </div>
        <h2>Nos présidents d’honneur</h2>
      </div>
    </section>

    <section class="partners-container">
      <div class="container">
        <h2>Nos partenaires</h2>
      </div>
    </section>
  </div>
</template>

<script>
import Card from './components/Card.vue'
import Navbar from './components/Navbar.vue'
import CardHorizontal from './components/CardHorizontal.vue'

export default {
  name: 'App',
  components: {
    Card,
    Navbar,
    CardHorizontal
  },
  data() {
    return {
      covers: [
        {
          title: "L’Union européenne se lance dans la course au standard des obligations vertes, par Sylvie Schmitt",
          description: "Le 6 juillet 2021, la Commission européenne a rendu publique sa stratégie de promotion de la finance durable. Deux projets de textes ont été présentés à cette occasion. Le premier …",
          daytime: "10 août 2021",
          src: require("@/assets/images/article-cover.png"),
          tag: "L’actualité au prisme du droit"
        }
      ],
      articles: [
        {
          title: "L’Union européenne se lance dans la course au standard des obligations vertes, par Sylvie Schmitt",
          description: "Le vote de la loi sous la Ve République est un exercice juridique convenu dont les acteurs sont identifiés et la conclusion souvent connue à l’avance.",
          daytime: "10 août 2021",
          src: require("@/assets/images/img-conseil-constitutionnel.png"),
          tag: "L’actualité au prisme du droit"
        },
        {
          title: "Le Tribunal constitutionnel espagnol censure l’état d’alarme : Vice juridique ou erreur politique ?",
          description: "L’information a filtré et elle a fait l’effet d’une bombe : le 14 juillet dernier, l’assemblée plénière du Tribunal constitutionnel espagnol a partiellement fait droit au recours d’inconstitutionnalité formé par le parti politique",
          daytime: "10 août 2021",
          src: require("@/assets/images/img-spanish-flag.png"),
          tag: "L’actualité au prisme du droit"
        }
      ],
      members: [
        {
          title: "Elisabeth Baraduc",
          description: "Avocat au Conseil d’Etat et à la Cour de cassation - Baraduc&Duhamel",
          src: require("@/assets/images/elisabeth_baraduc.png"),
          alt: "Portrait d'Elisabeth Baraduc"
        },
        {
          title: "Christine Lagarde",
          description: "Présidente de la Banque centrale européenne (BCE)",
          src: require("@/assets/images/christine_lagarde.png"),
          alt: "Portrait de Christine Lagarde"
        },
        {
          title: "Alexandre de Juniac",
          description: "Directeur Général de l’Association Internationale du Transport Aérien",
          src: require("@/assets/images/alexandre_de_juniac.png"),
          alt: "Portrait d'Alexandre de Juniac",
          class: "bw-hover"
        }
      ],
      news: [
        {
          title: "Sanctions internationales, par Gaëlle Filhol et Alexandre Reynaud",
          description: "Le recours aux sanctions internationales – comme celles adoptées en 2021 par les Etats-Unis contre des entreprises chinoises spécialisées dans la défense et les technologies de surveillance1 – ne cesse de croître et, dès lors, d’occuper l’actualité de l’arbitrage international.",
          src: require("@/assets/images/video1.png"),

        },
        {
          title: "Sanctions internationales, par Gaëlle Filhol et Alexandre Reynaud",
          description: "Le recours aux sanctions internationales – comme celles adoptées en 2021 par les Etats-Unis contre des entreprises chinoises spécialisées dans la défense et les technologies de surveillance1 – ne cesse de croître et, dès lors, d’occuper l’actualité de l’arbitrage international.",
          direction: "card img-right",
          src: require("@/assets/images/video2.png"),

        }
      ]
    }
  },
}
</script>

<style lang="stylus">
body 
  margin 0
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
.members-container
  padding 70px 166px 50px
  background-color #ffb563
  color #FFFFFF
.members-container h2
  font-size: 55px;
.members-container .card__description
  color #FFFFFF !important

.members-container button
  width: 299px;
  height: 64px;
  margin: 70px 54px 0 55px;
  padding: 20px 15px;
  background-color: #fff;
  border none
  margin 0 auto
.news-container
  background-color: #f2f2f2;

.news-container
  padding: 150px 152px 409px 165px;
  h2
    font-family: Seshat;
    font-size: 55px;
    margin 0 0 50px 0
  img
    width: 525px;
  .card
    margin-bottom 121px
.partners-container 
  padding-top 337px
  h2  
    font-family: Seshat;
    font-size: 55px;
</style>
