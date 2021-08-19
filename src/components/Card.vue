<template>
  <div class="card">
    <img :src="src" :alt="alt" :class="class_img">
    <p class="card__tag"><span>{{ tag }}</span></p>
    <p class="card__time"><time :datetime="daytime">{{ daytime }}</time></p>
    <h2 class="card__title">{{ title }}</h2>
    <p class="card__description">{{ description }}</p>
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
      class_img: String
    }
    
  }
</script>

<style lang="stylus" scoped>
.card

  .card__tag
    width 246px
    background-color #F2F2F2
    color #2D2D2D
  .card__time
    color #2D2D2D
    font-size 14px
    font-weight bold
    text-transform uppercase
  .card__title
    font-size 30px
  .card__description
    color #8D8D8D
</style>