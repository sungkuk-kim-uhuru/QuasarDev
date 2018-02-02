<template>
  <div class="row col-12 input-div">
    <q-input v-model="email" type="email" float-label="Email" suffix="@gmail.com"
    clearable class="full-width" />
    <q-input v-model="password" type="password" float-label="Password" clearable
    class="full-width" />
    <q-input v-if="pageName == 'join'" v-model="password2" type="password"
    float-label="Password 確認" clearable class="full-width" />
  </div>
</template>

<script>
  import {
    QInput
  } from 'quasar'

  export default{
    name: 'LoginBoxContent',
    props: ['pageName', 'email', 'password', 'password2'],
    components: {
      QInput
    }
  }
</script>

<style lang="scss" scoped>
  .q-if {
      padding: 0;
      margin: 0;
      height: 32px;
  }

  .login{
    .input-div{
      padding-top: 20px;
    }
  }
  .input-div{
    margin-top: 5px;
    margin-bottom: 5px;
    height: 175px;
    .q-if{
      margin-top: 5px;
      margin-bottom: 5px;
    }
  }
</style>
