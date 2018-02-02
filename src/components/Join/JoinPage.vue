<template>
  <q-layout
    ref="layout"
    view="lHh Lpr fff"
    :left-class="{'bg-grey-2': true}"
    class="bg-grey"
  >
    <LoginBox :page-name="pageName" ></LoginBox>
  </q-layout>
</template>

<script>
import LoginBox from '../Login/LoginBox.vue'

import {
  QLayout
} from 'quasar'

export default {
  name: 'JoinPage',
  components: {
    QLayout,
    LoginBox
  },
  data () {
    return {
      pageName: 'join'
    }
  },
  methods: {
    progressLoading (router) {
      setTimeout(function () {
        router.push('/Index')
      }, 1000)
    }
  },
  mounted () {

  },
  beforeDestroy () {

  }
}
</script>

<style lang="scss" scoped>

</style>
