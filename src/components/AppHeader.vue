<script>

import AppNavbar from './AppNavbar.vue';
import AppNavIcone from './AppNavIcone.vue';
import arrayNavbar from '../assets/data/arrayNavbar'
import arrayIcone from '../assets/data/arrayIcone'
import arrayCategory from '../assets/data/arrayCategory';
  export default {
    components:{
        AppNavbar,
        AppNavIcone
    },
    data(){
        return{
            listaNav: arrayNavbar,
            listaIcone: arrayIcone,
            listaCategorie: arrayCategory
        }

    }
      
  }
</script>
<template lang="">
  <header>
    <div class="container-fluid padding-container">
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
    <div class="container-fluid border-top"></div>
    <div class="container-fluid padding-container">
        <div class="row">
            <div class="col-12">
                <img src="../assets/img/masterstudy-logo.svg">

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

    
    .padding-container{
        padding: 1rem 7rem 0rem;
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