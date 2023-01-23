<script>

import AppNavbar from './AppNavbar.vue';
import AppNavIcone from './AppNavIcone.vue';
import arrayNavbar from '../assets/data/arrayNavbar'
import arrayIcone from '../assets/data/arrayIcone'
  export default {
    components:{
        AppNavbar,
        AppNavIcone
    },
    data(){
        return{
            listaNav: arrayNavbar,
            listaIcone: arrayIcone
        }

    }
      
  }
</script>
<template lang="">
  <header>
    <div class="container-fluid padding-header">
        <div class="row navbar ">
            <div class="col-2 ">
                English
            </div>
            <div class="col-10 d-flex justify-content-end">
                <ul class="list-unstyled d-flex">
                    <AppNavbar v-for="(item, index) in listaNav" :key="index" :navbar="item"></AppNavbar>
                </ul>
                <ul  class="list-unstyled d-flex lista-icone">
                    <AppNavIcone v-for="(item, index) in listaIcone" :key="index" :icone="item"></AppNavIcone>
                </ul>
            </div>

        </div>
        
    </div>
    <div class="container-fluid border-top">

    </div>
  </header>
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

header{
    height: 250px;
    width: 100%;

    
    .padding-header{
        padding: 1rem 7rem;
        .navbar{
        color: $colorGrey;
        font-size: 14px;

        .lista-icone{
            margin-left: 2rem;
        }

    }

    }


}
  
</style>