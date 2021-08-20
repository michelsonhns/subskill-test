<template>
  <div>
    <nav>
      <div class="nav-brand">
        <img src="../assets/logos/logo-avocats-de-france.png" alt="">
      </div>
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
nav
  display flex
  align-items center;
  padding: 16px 282px 17px 48px;
  border-bottom solid 1px #efefef


nav ul
  display flex
  margin 0 auto

nav ul li
  padding-left 30px
  margin 0 30px
nav ul li:first-child
  list-style none
img
  width 75px

</style>