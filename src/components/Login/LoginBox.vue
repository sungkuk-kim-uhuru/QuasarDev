<template>
  <div class="row bg-white fixed-center login-box" v-bind:class="pageName" >
    <LoginBoxHeader v-bind:header-title="pageName=='login' ? 'ログイン' : '会員登録'">
    </LoginBoxHeader>

    <LoginBoxContent v-bind:page-name="pageName" v-bind:email="email"
    v-bind:password="password" v-bind:password2="password2"></LoginBoxContent>

    <LoginBoxFooter v-bind:page-name="pageName" v-on:login="progressLoading($router)"></LoginBoxFooter>
  </div>
</template>
<script>
import LoginBoxHeader from './LoginBoxHeader.vue'
import LoginBoxContent from './LoginBoxContent.vue'
import LoginBoxFooter from './LoginBoxFooter.vue'

export default {
  name: 'LoginBox',
  props: ['pageName'],
  components: {
    LoginBoxHeader,
    LoginBoxContent,
    LoginBoxFooter
  },
  data () {
    return {
      email: 'defaultEmail',
      password: 'defaultPassword',
      password2: 'defaultPassword'
    }
  },
  methods: {
    progressLoading (router) {
      setTimeout(function () {
        router.push('/Index')
      }, 1000)
    }
  }
}
</script>
<style lang="scss" scoped>

.login-box{
  width:90%;
  max-width: 400px;
  height: 320px;
  padding:20px;

}

</style>
