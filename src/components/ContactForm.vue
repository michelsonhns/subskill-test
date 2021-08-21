<template>
  <div class="contact-form">
    <div class="form-group">
      <div class="form-input">
        <label for="">Nom <span>*</span></label>
        <input type="text" name="" id="" placeholder="Votre nom">
      </div>
      <div class="form-input">
        <label for="">Prénom <span>*</span></label>
        <input type="text" name="" id="" placeholder="Votre prénom">
      </div>
    </div>
    <div class="form-group">
      <div class="form-input">
        <label for="">Email <span>*</span></label>
        <input type="text" name="" id="" placeholder="Votre Email">
      </div>
      <div class="form-input">
        <label for="">Destinataire de ce message <span>*</span></label>
        <select name="" id="">
          <option value="">Séléctionner le déstinataire</option>
        </select>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="stylus" scoped>
.contact-form
  padding 30px 0
  label
    display block
    margin 1em 0
  input, select
    border none
    border-bottom solid 1px #dcdcdc
    width 100%


.form-group
  display flex
  flex-direction column

@media (min-width: 800px)
  .form-input:first-child
    margin-right 2em
  .form-input
    width 50%
  .form-group
    flex-direction row
</style>