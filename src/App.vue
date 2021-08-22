<template>
  <div>
    <header>
      <Navbar/>
    </header>
    <main>
      <section class="cover__container">
        <div class="container">
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
        </div>
        
      </section>

      <section class="articles__container">
        <div class="article__group container">
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
            :src="newsletter.src"
            :daytime="newsletter.daytime">
              <Button title="Découvrir l’article" btnclass="yellow"/>
            </Card>
            
          </div>
          <h2 class="section__title">Le club des juristes</h2>
          <aside>
            <p>Créé en 2007, le Club des juristes est <span class="bold">le premier think tank juridique français</span>. Il s’agit d’un lieu indépendant de réflexion sur la place du droit en France. <span class="bold">Le « Club » a pour objectif de nourrir le débat public</span> en formulant des propositions concrètes dans le domaine du droit et de la justice. C’est notamment le travail des commissions – justice, fiscalité, environnement, constitutions et institutions, Europe, et commissions dites « ad hoc » – qu’il réunit en son sein et qui aboutissent à des recommandations innovantes, utiles aux décideurs publics. Pour ce faire, <span class="bold">le Club des juristes réunit des professionnels du droit reconnus issus d’horizons divers : avocats, magistrats, notaires, universitaires, représentants d’entreprises, etc</span>.</p>
            <Button
              title="En savoir plus"
               btnclass="white"/>
          </aside>
        </div>
      </section>

      <section class="partners__container">
        <div class="container">
          <h2 class="section__title">Nos partenaires</h2>
          <Partners/>
          <div class="cta">
            <Button title="Voir tous les partenaires" btnclass="yellow"/>
          </div>
        </div>
      </section>

      <section class="videos__section">
        <div class="container">
          <h2 class="section__title">Dernières vidéos du club</h2>
        </div>
        <Carousel/>
      </section>

      <section class="contact__container">
        <div class="container">
          <h2 class="section__title">Nous contacter</h2>
          <span class="help-text">Afin de traiter votre demande dans les plus brefs délais, nous vous invitons à utiliser le formulaire ci-dessous.</span>
          <p>Attention : Le Club des juristes n’est pas un cabinet d’avocats, il n’est pas en mesure de répondre aux questions portant sur des situations personnelles. Nous vous invitons pour cela à vous adresser directement aux professionnels concernés. Merci pour votre compréhension.</p>
          <ContactForm/>
        </div>
      </section>
    </main>
    <Footbar/>
  </div>

</template>

<script>
import Card from './components/Card.vue'
import Navbar from './components/Navbar.vue'
import Footbar from './components/Footbar.vue'
import Partners from './components/Partners.vue'
import Button from './components/Button.vue'
import ContactForm from './components/ContactForm.vue'
import Carousel from './components/Carousel.vue'

export default {
  name: 'App',
  components: {
    Card,
    Navbar,
    Partners,
    Button,
    ContactForm,
    Footbar,
    Carousel
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
          daytime: "10 août 2021",

        },
        {
          title: "Sanctions internationales, par Gaëlle Filhol et Alexandre Reynaud",
          description: "Le recours aux sanctions internationales – comme celles adoptées en 2021 par les Etats-Unis contre des entreprises chinoises spécialisées dans la défense et les technologies de surveillance1 – ne cesse de croître et, dès lors, d’occuper l’actualité de l’arbitrage international.",
          positioning: "horizontal img-right",
          src: require("@/assets/images/video2.png"),
          daytime: "10 août 2021",

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
  font-family 'Poppins', sans-serif

.bold
  font-weight bold

.container {
  width 95%
  margin 0 auto
}

.section__title
  font-size: 3.43em;
  margin-bottom 50px
  font-weight normal
  font-family "Seshat", sans-serif

.cta 
  text-align center

.cover__container
  background url("./assets/icons/round-black.png") bottom 285px right 0 / 110px no-repeat
  .card 
    width 100%
    img
      max-width 100%

.article__group
  .card 
    img
      max-width 100%

.members__container
  background-image url("./assets/icons/round-bicolor.png")
  background-repeat no-repeat
  background-position: bottom -102px right 20px;
  background-size: 190px;
  padding: 70px 0;
  background-color #ffb563
  font-stretch normal
  color #FFFFFF
  .card__description, .card__title
    color #FFFFFF !important

.news__container
  padding: 39px 0;
  background-color: #f2f2f2;
  .card 
    img
      max-width 100%

.news__container
  background  url("./assets/icons/round-bicolor.png")top -92px right 20px / 190px no-repeat,url("./assets/icons/round-green.png") bottom -127px left 30px / 218px no-repeat
  background-color #F2F2F2
  padding-bottom 150px

.help-text
  font-family Poppins
  font-size 0.87em
  color #2d2d2d

.contact__container
  p
    margin: 15px 0 50px;
    font-family: Poppins;
    font-size: 14px;
    font-weight: bold;
    font-style: italic;
    color: #2d2d2d;

aside
  background #b3dec1
  padding 30px;

.partners__container
  padding-top 100px
  margin-bottom 160px
  background url("./assets/icons/round-green.png") top -115px left 30px / 218px no-repeat

// Desktop
@media (min-width: 1131px)
  .container {
    width 80%
  }
  .article__group
    display flex
    justify-content space-between
    .card 
      width 526px
      img
        max-width 100%
  
  .cover__container
    margin-top 51px
    background-position bottom 171px right 100px
    background-size 193px

  .news__container
    padding: 150px 0;
    background url("./assets/icons/round-bicolor.png") top -140px right 20px / 290px no-repeat, url("./assets/icons/round-green.png") bottom -127px left 30px / 218px no-repeat
    background-color #F2F2F2

  .partners__container
    margin-bottom 160px
    padding-top 337px
    background url("./assets/icons/round-green.png") top -116px left 30px / 218px no-repeat
    .cta
      margin-top 70px

  .members__container
    background-image url("./assets/icons/round-bicolor.png")
    background-repeat no-repeat
    background-position: bottom -155px right 20px;
    background-size: 290px;

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
  
  .videos__section
    padding: 70px 49px 70px 46px;
    background-color: #f2f2f2;

  aside
    padding 50px 57px 50px 59px;
    width: 40%;
    position absolute
    right 14%
  
  .contact__container
    margin-bottom 50px

</style>
