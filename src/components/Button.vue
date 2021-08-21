<template>
  <div>
    <a :href="href" class="button" :class="btnclass">{{ title }} <i class="fas fa-arrow-right"></i></a>
  </div>
</template>

<script>
  export default {
    props: {
      title: {
        type: String,
        default: "send"
      },
      href: {
        type: String,
        default: "#"
      },
      btnclass: {
        type: String,
        default: ""
      }
    },
    
  }
</script>

<style lang="stylus" scoped>
.button
  display: inline-block;
  padding: 20px 15px;
  text-decoration: none;
  border: none;
  transition: all 0.3s;
  position: relative;
  overflow: hidden;
  z-index: 1;
  i
    margin-left 0.80em

.button.yellow
    background-color: #ffb563;
    color: #2d2d2d;
.button.white
    background-color: #fff;
    color: #2d2d2d;

.button:before
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0%;
  height: 100%;
  background-color: #231f20;
  color: #231f20;
  transition: all 0.3s;
  z-index: -1;

.button:hover
  color: #FFFFFF;

.button:hover:before
  width: 100%;

</style>