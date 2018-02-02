<template>
  <div class="row col-12 login-text relative-position">
    <span class="absolute-center">{{headerTitle}}</span>
  </div>
</template>

<script>
export default {
  name: 'LoginBoxHeader',
  props: ['headerTitle']
}
</script>

<style lang="scss" scoped>
  .login-text{
    height:40px;
    font-size:32px;
    text-align: center;
  }
</style>



