<template>
  <div class="contact-form">
    <div class="form-group">
      <div class="form-input">
        <label for="lastName">Nom <span>*</span></label>
        <input type="text" name="" id="lastName" placeholder="Votre nom">
      </div>
      <div class="form-input">
        <label for="firstName">Prénom <span>*</span></label>
        <input type="text" name="" id="firstName" placeholder="Votre prénom">
      </div>
    </div>
    <div class="form-group">
      <div class="form-input">
        <label for="email">Email <span>*</span></label>
        <input type="text" name="" id="email" placeholder="Votre Email">
      </div>
      <div class="form-input">
        <label for="recipient">Destinataire de ce message <span>*</span></label>
        <select name="" id="recipient">
          <option value="">Séléctionner le déstinataire</option>
        </select>
      </div>
    </div>
    <div class="form-group">
      <div class="textarea">
        <label for="message">Message<span>*</span></label>
        <textarea name="" id="message" rows="3" placeholder="Votre message"></textarea>
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
    font-size 1.87em
    span
      color #ffb563
  input, select, textarea
    border none
    border-bottom solid 1px #dcdcdc
    padding-bottom 5px
    width 100%
  ::placeholder, select
    font-family sans-serif
    color: #848484;
    font-size 0.87em !important

.form-group
  display flex
  flex-direction column
input:focus , select:focus, textarea:focus
  outline none
@media (min-width: 1131px)
  .form-input:first-child
    margin-right 2em
  .form-input
    width 50%
  .textarea
    width 100%
  .form-group
    flex-direction row
</style>