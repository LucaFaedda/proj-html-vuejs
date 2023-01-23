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
    <div class="container">
        <div class="row">
            <div class="col-2">
                English
            </div>
            <div class="col-8 d-flex">
                <ul class="list-unstyled d-flex">
                    <AppNavbar v-for="(item, index) in listaNav" :key="index" :navbar="item"></AppNavbar>
                </ul>
            </div>
            <div class="col-2">

            </div>
        </div>

    </div>
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