<template>
  <div>
    <nav>
      <div class="nav-brand">
        <img src="../assets/logos/logo-avocats-de-france.png" alt="">
      </div>
      <button class="navbar-toggler" aria-label="Toggle navigation"><i class="fas fa-bars"></i></button>
      <ul>
        <li class="nav-item">Toute l’actu</li>
        <li class="nav-item">Le club</li>
        <li class="nav-item">Publication</li>
        <li class="nav-item">Nos partenaires</li>
        <li class="nav-item">Évènements</li>
      </ul>
    </nav>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="stylus" scoped>
img
  width 75px

nav
  display flex
  justify-content space-between
  align-items center;
  padding: 16px
  border-bottom solid 1px #efefef

  ul
    display none
  
  button
    background-color #FFF
    border none
    font-size 1.8em

@media (min-width: 1131px)
  nav
    padding: 16px 282px 17px 48px;
    button
      display none
  nav ul
    display flex
    margin 0 auto

  nav ul li
    padding-left 30px

  ul 
    list-style: none


  ul li::before 
    content: "•"
    margin-right 30px

  nav ul li:first-child::before 
    content: ""

</style>