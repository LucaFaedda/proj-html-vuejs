<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';
  export default {
      components:{
        AppHeader,
        AppFooter,
        AppMain
      }
  }
</script>
<template lang="">
  <div>
    <AppHeader></AppHeader>
    <AppMain></AppMain>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss">

@use './assets/style/general.scss' as *;
@use './assets/style/partials/mixin.scss' as *;
@use './assets/style/partials/variables.scss' as *;

  
</style>