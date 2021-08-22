<template>
  <div class="card" :class="positioning">
    <img :src="src" :alt="alt" :class="class_img">
    <div>
        <p class="card__tag" v-if="tag"><span>{{ tag }}</span></p>
        <p class="card__time"><time :datetime="daytime">{{ daytime }}</time></p>
        <h3 class="card__title" :class="class_title">{{ title }}</h3>
        <p class="card__description" :class="class_description">{{ description }}</p>
        <div class="slot__card">
          <slot></slot>
        </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      title: String,
      description: String,
      src: String,
      daytime: String,
      tag: String,
      alt: String,
      class_img: String,
      class_description: String,
      class_title: String,
      positioning: String,
      src: {
        type: String,
        default: require("@/assets/images/christine_lagarde.png")
      },
    }
    
  }
</script>

<style lang="stylus" scoped>
@font-face
  font-family Seshat
  font-style normal
  src url(../assets/fonts/seshat/Seshat.otf) format("opentype")
  
.card
  margin-bottom 70px
  .card__tag
    display inline-block
    background-color #F2F2F2
    font-family Poppins
    padding 7px 16px 7px 18px
  
  .card__tag, .card__time
    color #2D2D2D
    font-size 0.875em
    font-weight bold

  .card__time
    text-transform uppercase
    line-height 1.5
    letter-spacing 1px
  
  .card__title
    font-size 1.875em
    font-family 'Seshat', sans-serif
    color #2d2d2d
    margin 10px 0

  .card__description
    color #8D8D8D
    margin 0

  .slot__card
    margin-top 1.8em

    
@media (min-width: 1131px)
  .is-three-quarters
    width: 759px;
  
  .is-half
    width: 642px;

  .horizontal 
    display flex
    img
      width: 525px;
      margin: 0 57px 0 0;

  .img-right
    flex-direction row-reverse
    img
      width: 525px;
      margin: 0 57px 0 0;
</style>