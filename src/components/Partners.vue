<template>
  <div class="">
    <div class="row">
      <div class="card-logo">
        <img src="@/assets/logos/logo-accor-hotels.png" alt="">
      </div>
      <div class="card-logo">
        <img src="@/assets/logos/logo-air-france-klm.png" alt="">
      </div>
      <div class="card-logo">
        <img src="@/assets/logos/logo-france-tv.png" alt="">
      </div>
    </div>
    <div class="row">
      <div class="card-logo">
        <img src="@/assets/logos/logo-carrefour.png" alt="">
      </div>
      <div class="card-logo">
        <img src="@/assets/logos/logo-edf.png" alt="">
      </div>
      <div class="card-logo">
        <img src="@/assets/logos/logo-loreal.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    
  }
</script>

<style lang="stylus" scoped>
.card-logo
  width 100%
  margin 0 31px 30px 0
  box-shadow 0 3px 10px 0 rgba(212, 212, 212, 0.5)
  background-color #fff
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  img
    margin 48px auto
    width: 168px
  
.card-logo:hover
  background-color #0d2d99
  transition: all 1.1s ease-out;


.row
  justify-content space-around
  button
    padding: 20px 15px;
    background-color: #ffb563;
    border none
    i
      margin-left 0.80em

@media (min-width: 1131px)
  .row
    display flex
  .card-logo
    width 33%
    display: flex;
</style>

