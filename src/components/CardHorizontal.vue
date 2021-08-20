<template>
  <div :class="direction">
    <img :src="src" :alt="alt" :class="class_img">
    <div>
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      title: {
        type: String,
        default: "title" 
      },
      description: {
        type: String,
        default: "description" 
      },
      direction: {
        type: String,
        default: "flex card" 
      },
      src: {
        type: String,
        default: require("@/assets/images/christine_lagarde.png")
      },
      alt: {
        type: String,
        default: "image"
      },
    },
  }
</script>

<style lang="stylus" scoped>

.flex 
  display flex
.img-right
  display flex
  flex-direction row-reverse
h3
  width: 540px;
  font-family: Seshat;
  font-size: 30px;
  color: #2d2d2d;
p
  font-family: Poppins;
  font-size: 14px;
  line-height: 1.5;
  letter-spacing: 1px;
  color: #8d8d8d;
img
  width: 525px;
  margin: 0 57px 0 0;

</style>