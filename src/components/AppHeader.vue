<script>

import AppNavbar from './AppNavbar.vue';
import AppNavIcone from './AppNavIcone.vue';
import AppCategoryBar from './AppCategoryBar.vue';
import arrayNavbar from '../assets/data/arrayNavbar'
import arrayIcone from '../assets/data/arrayIcone'
import arrayCategory from '../assets/data/arrayCategory';
  export default {
    components:{
        AppNavbar,
        AppNavIcone,
        AppCategoryBar
    },
    data(){
        return{
            listaNav: arrayNavbar,
            listaIcone: arrayIcone,
            listaCategorie: arrayCategory,
            isOpen: false
        }

    },
    methods: {
        onOver(){
            this.isOpen = true
        },
        onLeave(){
            this.isOpen = false
        }
    },
      
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
            <div class="col-12 d-flex align-items-center ">
                <img src="../assets/img/masterstudy-logo.svg">
                <div class="d-flex align-items-center ms-4">
                    <button class="navbar-toggler" type="button" data-mdb-toggle="collapse"
                    data-mdb-target="#navbarToggleExternalContent" aria-controls="navbarToggleExternalContent"
                    aria-expanded="false" aria-label="Toggle navigation">
                    <i class="fas fa-bars"></i>
                    </button>
                    <span
                        v-on:mouseover="onOver"
                        v-on:mouseleave="onLeave" class="contenitore-dropdown ms-1">
                        Category
                        
                        <ul class=" menu-discesa"
                           :class="{ isOpen }">
                            <AppCategoryBar v-for="(item, index) in listaCategorie" :key="index" :categoria="item"/>
                        </ul>
                    </span>
                </div>
                <div class="input-container d-flex align-items-center mx-4">
                    <input type="text"  placeholder="Search Course" aria-label="Recipient's username"  >
                    <button class="btn btn-personalizzato"  ><i class="fa-solid fa-magnifying-glass"></i></button>
                </div>
                <div class="container-icone ms-4">
                    <i class="fa-solid fa-bullhorn "></i>
                    <span>Become an Instructor</span>
                </div>
                <div class="container-icone ms-4">
                    <i class="fa-solid fa-briefcase"></i>
                    <span>For Enterprise</span>
                </div>
                <div class="sign-up ms-5">
                    <i class="fa-regular fa-user "></i>
                    <span>Log in</span>
                    <button class="btn btn-danger mx-3">SIGN UP</button>
                    <i class="fa-regular fa-heart "></i>
                </div>
            </div>
            <!-- <div class="col-4  d-flex align-items-center ">
            </div>
            <div class="col-3 d-flex align-items-center">
            </div> -->
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
.contenitore-dropdown{
    position: relative;
}
.menu-discesa{
    position: absolute;
    top: 100%;
    left: 0;
    display: none;
    padding: 0;
    list-style-type: none;
}

.isOpen {
    display: block;
}

.input-container{
    input{
        width: 500px;
        border: none;
        padding: 9px 20px;
        background-color: #f0f2f5;

    }

}


.btn-personalizzato{
    border-radius: 0;
    background-color: $colorLightblu;
    color: #fff;
    padding:8px 20px;

    &:hover{
        cursor: pointer;
        background-color: $colorLightblu;
        color: #fff;
    }

}



  
</style>