<script>

import AppNavbar from './AppNavbar.vue';
import arrayNavbar from '../assets/data/arrayNavbar'
  export default {
    components:{
        AppNavbar
    },
    data(){
        return{
            listaNav: arrayNavbar
        }

    }
      
  }
</script>
<template lang="">
  <header>
    <AppNavbar></AppNavbar>
  </header>
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

header{
    height: 250px;
    width: 100%;
}
  
</style>