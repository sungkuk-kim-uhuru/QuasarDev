<template>
  <div class="row col-12 xs-gutter btn-div no-margin relative-position">
    <div class="col-6" v-if="pageName=='login'">
      <q-btn loader color="primary" class="full-width" @click="login" >ログイン</q-btn>
    </div>
    <div class="col-6" v-if="pageName=='login'">
      <q-btn color="primary" class="full-width" @click="$router.push('/Join')">
        会員登録
      </q-btn>
    </div>
    <div class="col-12" v-if="pageName=='join'">
      <q-btn color="primary" class="full-width " @click="$router.push('/')" >
        会員登録
      </q-btn>
    </div>
  </div>
</template>

<script>
  import {
    QBtn
  } from 'quasar'

  export default {
    name: 'LoginBoxContent',
    props: ['pageName'],
    components: {
      QBtn
    },
    methods: {
      login: function () {
        console.log('emit!!')
        this.$emit('login')
      }
    }
  }
</script>

<style lang="scss" scoped>
  .btn-div{
    .q-btn{
      font-weight: bold;
      height: 36px;
      a{
        color:white;
      }
    }
  }
</style>





