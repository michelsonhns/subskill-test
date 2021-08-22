<template>
  <footer>
    <div class="footer-brand">
      <img src="../assets/logos/logo-avocats-de-france.png" alt="">
    </div>
    <ul>
      <li class="footer-item">Toute l’actu</li>
      <li class="footer-item">Le club</li>
      <li class="footer-item">Publication</li>
      <li class="footer-item">Nos partenaires</li>
      <li class="footer-item">Évènements</li>
    </ul>
  </footer>
</template>

<script>
  export default {
    
  }
</script>

<style lang="stylus" scoped>
img
  width 75px

footer
  background-color #f2f2f2
  display flex
  justify-content space-between
  align-items center;
  padding: 16px
  border-bottom solid 1px #efefef
  
  ul 
    list-style: none

@media (min-width: 1131px)
  footer
    padding: 112px

  footer ul
    display flex
    margin 0 auto

  footer ul li
    padding-left 30px



</style>