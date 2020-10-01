<template lang="pug">
  #app
    div.col(v-for="user in users")
      UserCard(
        :avatar='user.avatar'
        :username='user.username'
        :email='user.email'
      )
</template>

<script>
import UserCard from './components/UserCard.vue';

export default {
  name: 'App',
  components: {
    UserCard,
  },
  data() {
    return {
      users: [
        {
          avatar: 'https://avatars0.githubusercontent.com/u/29035007?s=460&u=d43c9fdb7ae872c84a38aa6a0c04db49cb7e59f4&v=4',
          username: 'Martins Onuoha',
          email: 'martinsvictor.nd@gmail.com',
        },
        {
          avatar: 'https://avatars2.githubusercontent.com/u/2798204?s=460&u=d5b35f5a43986232e2d226539071ec1008db5166&v=4',
          username: 'Guillaume Chau',
          email: 'guillaume.b.chau@gmail.com',
        },
        {
          avatar: 'https://avatars3.githubusercontent.com/u/499550?s=460&u=de41ec9325e8a92e281b96a1514a0fd1cd81ad4a&v=4',
          username: 'Evan You',
          email: 'evan@you.com',
        },
        {
          avatar: 'https://avatars2.githubusercontent.com/u/3277634?s=460&v=4',
          username: 'Haoqun Jiang',
          email: '@haoqunjiang',
        },
      ],
    };
  },
};
</script>

<style lang="stylus">
body
  background-color: #FFF4EC
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  display flex
  justify-content: center;
  text-align: center
  margin-top: 60px
  .col
    width 100%
</style>
