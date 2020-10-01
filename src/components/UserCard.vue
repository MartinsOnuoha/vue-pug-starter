<template lang="pug">
  .user-card-component
    .user-card-component__avatar
      img(:src='`${avatar}`' class='user-card-component__avatar-image')

    .user-card-component__name {{ username }}

    .user-card-component__email {{ email }}

    .user-card-component__action
      button(@click="$emit('contactUser')") Contact {{ lastName }}
</template>

<script>
export default {
  name: 'user-card-component',
  props: {
    avatar: {
      type: String,
      default: '',
    },
    username: {
      type: String,
      default: 'Martins Onuoha',
    },
    email: {
      type: String,
      default: 'martinsvictor.nd@gmail.com',
    },
  },
  computed: {
    lastName() {
      return this.username.split(' ')[1];
    },
  },
};
</script>

<style lang="stylus">
  shdw = 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.2)

  .user-card-component
    box-shadow shdw;
    background-color #ffffff
    border-radius 10px
    padding 10px
    width 70%
    margin 0 auto
    &__avatar
      &-image
        border-radius 50%
        width 6rem
    &__email
      font-size 15px
      padding 10px
      color #CCC
    &__name
      font-size: 20px
      font-weight 500
    button
      padding 8px
      background #4DB6AC
      color #FFF
      width 80%
      border-radius 5px
      box-shadow shdw
      border 0
    .spacer
      border-color #CCC
</style>
