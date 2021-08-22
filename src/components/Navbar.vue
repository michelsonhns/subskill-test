<template>
  <div>
    <nav>
      <div class="nav-brand">
        <img src="../assets/logos/logo-avocats-de-france.png" alt="">
      </div>
      <button class="navbar-toggler" aria-label="Toggle navigation"><i class="fas fa-bars"></i></button>
      <ul>
        <li class="nav-item"><a href="#">Toute l’actu</a></li>
        <li class="nav-item"><a href="#">Le club</a></li>
        <li class="nav-item"><a href="#">Publication</a></li>
        <li class="nav-item"><a href="#">Nos partenaires</a></li>
        <li class="nav-item"><a href="#">Évènements</a></li>
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
  a 
    text-decoration none
    color #2d2d2d


@media (min-width: 1131px)
  nav
    padding: 16px 282px 17px 48px;
    button
      display none
    ul
      display flex
      margin 0 auto
      list-style: none
      li
        padding-left 30px
        a:hover
          font-weight: 400;
          text-decoration underline
      :first-child::before 
        content: ""
      ::before 
        content: "•"
        margin-right 30px
</style>