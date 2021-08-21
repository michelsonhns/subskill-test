<template>
  <main>
    <Navbar/>
    <div class="container">
      <section class="cover__container">
        <Card 
            v-for="article in covers" :key="article.id"
            :title="article.title"
            :daytime="article.daytime"
            :description="article.description"
            :src="article.src"
            :tag="article.tag"
            :class_description="article.class_description"
            :class_title="article.class_title"
          />
      </section>
      <section class="articles-container">
        <div class="article-group">
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
    <section class="members__container">
      <div class="container">
        <h2 class="section__title">Nos présidents d’honneur</h2>
        <div class="members__wrap">
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
          <div class="cta">
            <Button title="Découvrir les membres du club" btnclass="white"/>
          </div>
      </div>
    </section>

    <section class="news__container">
      <div class="container">
        <h2 class="section__title">La semaine juridique</h2>
        <div class="card-group">
          <Card
          v-for="newsletter in news" :key="newsletter.id"
          :title="newsletter.title"
          :description="newsletter.description"
          :positioning="newsletter.positioning"
          :src="newsletter.src">
            <Button title="Découvrir l’article" btnclass="yellow"/>
          </Card>
          
        </div>
        <h2 class="section__title">Nos présidents d’honneur</h2>
      </div>
    </section>

    <section class="partners-container">
      <div class="container">
        <h2 class="section__title">Nos partenaires</h2>
        <Partners/>
        <div class="cta">
          <Button title="Voir tous les partenaires" btnclass="yellow"/>
        </div>
      </div>
    </section>

    <section class="contact-container">
      <div class="container">
        <h2 class="section__title">Nous contacter</h2>
        <span class="help-text">Afin de traiter votre demande dans les plus brefs délais, nous vous invitons à utiliser le formulaire ci-dessous.</span>
        <p>Attention : Le Club des juristes n’est pas un cabinet d’avocats, il n’est pas en mesure de répondre aux questions portant sur des situations personnelles. Nous vous invitons pour cela à vous adresser directement aux professionnels concernés. Merci pour votre compréhension.</p>
        <ContactForm/>
      </div>
    </section>
  </main>
</template>

<script>
import Card from './components/Card.vue'
import Navbar from './components/Navbar.vue'
import Partners from './components/Partners.vue'
import Button from './components/Button.vue'
import ContactForm from './components/ContactForm.vue'

export default {
  name: 'App',
  components: {
    Card,
    Navbar,
    Partners,
    Button,
    ContactForm
  },
  data() {
    return {
      covers: [
        {
          title: "L’Union européenne se lance dans la course au standard des obligations vertes, par Sylvie Schmitt",
          description: "Le 6 juillet 2021, la Commission européenne a rendu publique sa stratégie de promotion de la finance durable. Deux projets de textes ont été présentés à cette occasion. Le premier …",
          daytime: "10 août 2021",
          src: require("@/assets/images/article-cover.png"),
          tag: "L’actualité au prisme du droit",
          class_description: "is-half",
          class_title: "is-three-quarters"
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
          title: "Le Tribunal constitutionnel espagnol censure l’état d’alarme: Vice juridique ou erreur politique?",
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
          positioning: "horizontal",
          src: require("@/assets/images/video1.png"),

        },
        {
          title: "Sanctions internationales, par Gaëlle Filhol et Alexandre Reynaud",
          description: "Le recours aux sanctions internationales – comme celles adoptées en 2021 par les Etats-Unis contre des entreprises chinoises spécialisées dans la défense et les technologies de surveillance1 – ne cesse de croître et, dès lors, d’occuper l’actualité de l’arbitrage international.",
          positioning: "horizontal img-right",
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
  font-size 100%
  font-family: 'Poppins', sans-serif;

.container {
  width 80%
  margin 0 auto
}

.section__title
  font-size: 1.87em;
  margin-bottom 50px

.cta 
  text-align center

.cover__container
  .card 
    width 100%
    img
      max-width 100%

.article-group
  .card 
    img
      max-width 100%

  
.members__container
  padding: 70px 0;
  .card__title
    color #FFFFFF !important
  background-color #ffb563
  color #FFFFFF
  .section__title
    font-size 

.members__container .card__description
  color #FFFFFF !important

.members__container button
  width: 299px;
  height: 64px;
  margin: 70px 54px 0 55px;
  padding: 20px 15px;
  background-color: #fff;
  border none
  margin 0 auto


.news__container
  padding: 150px 0;
  background-color: #f2f2f2;
  .card 
    img
      max-width 100%

.partners-container 
  padding-top 337px

.help-text
  font-family Poppins
  font-size 0.87em
  color #2d2d2d
.contact-container
  p
    margin: 15px 0 50px;
    font-family: Poppins;
    font-size: 14px;
    font-weight: bold;
    font-style: italic;
    color: #2d2d2d;


@media (min-width: 800px)
  .article-group
    display flex
    justify-content space-between
    .card 
      width 526px
      img
        max-width 100%
  
  .members__wrap
    display flex
    justify-content space-between
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
