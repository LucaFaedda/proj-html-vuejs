<script>

import AppNavbar from './ComponentsAppHeader/AppNavbar.vue';
import AppNavIcone from './ComponentsAppHeader/AppNavIcone.vue';
import AppCategoryBar from './ComponentsAppHeader/AppCategoryBar.vue';
import AppCorsi from './ComponentsAppHeader/AppCorsi.vue';
import arrayNavbar from '../assets/data/arrayNavbar'
import arrayIcone from '../assets/data/arrayIcone'
import arrayCategory from '../assets/data/arrayCategory';
import arrayCourses from '../assets/data/arrayCourses';
  export default {
    components:{
        AppNavbar,
        AppNavIcone,
        AppCategoryBar,
        AppCorsi
    },
    data(){
        return{
            listaNav: arrayNavbar,
            listaIcone: arrayIcone,
            listaCategorie: arrayCategory,
            listaCorsi: arrayCourses,
            isOpen: false,
            selected: ''
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
        <!-- inizio navbar -->
        <div class="container-fluid padding-container">
            <div class="row navbar ">
                <div class="col-2 ">
                    <select v-model="selected">
                        <option>English</option>
                        <option>Deutesch</option>
                        <option>Italian</option>
                    </select>
                </div>
                <div class="col-10 d-flex justify-content-end">
                    <div class=" d-flex" >
                        <AppNavbar v-for="(item, index) in listaNav" :key="index" :navbar="item"></AppNavbar>
                    </div>
                    <div  class=" mx-2 lista-icone">
                        <AppNavIcone v-for="(item, index) in listaIcone" :key="index" :icone="item"></AppNavIcone>
                    </div>
                </div>
            </div>
        </div>
        <!-- inizio searchbar -->
        <div class="container-fluid border-top"></div>
        <div class="container-fluid padding-container">
            <div class="row mt-3">
                <div class="col-12 d-flex align-items-center justify-content-between">
                    <img src="../assets/img/masterstudy-logo.svg">
                    <div class="d-flex align-items-center">
                        <button class="navbar-toggler" type="button" data-mdb-toggle="collapse"
                        data-mdb-target="#navbarToggleExternalContent" aria-controls="navbarToggleExternalContent"
                        aria-expanded="false" aria-label="Toggle navigation">
                        <i class="fas fa-bars"></i>
                        </button>
                        <span
                            v-on:mouseover="onOver"
                            v-on:mouseleave="onLeave" class="contenitore-dropdown ms-1">
                            Category
                            
                            <span class=" menu-discesa"
                            :class="{ isOpen }">
                                <AppCategoryBar v-for="(item, index) in listaCategorie" :key="index" :categoria="item"/>
                            </span>
                        </span>
                    </div>
                    <div class="input-container d-flex align-items-center ">
                        <input type="text"  placeholder="Search Course" aria-label="Recipient's username"  >
                        <button class="btn btn-personalizzato"  ><i class="fa-solid fa-magnifying-glass"></i></button>
                    </div>
                    <div class="container-icone">
                        <i class="fa-solid fa-bullhorn me-2"></i>
                        <span>Become an Instructor</span>
                        <i class="fa-solid fa-briefcase me-2 ms-4"></i>
                        <span>For Enterprise</span>
                    </div>
                    <div class="sign-up ">
                        <i class="fa-regular fa-user me-2"></i>
                        <span>Log in</span>
                        <button class="btn btn-sign-up mx-3">SIGN UP</button>
                        <i class="fa-regular fa-heart "></i>
                    </div>
                </div>
            </div>
        </div>
        <!-- sezione corsi -->
        <div class="container-fluid bk-blue mt-4">
            <div class="d-flex justify-content-center  container-small">
                <AppCorsi  v-for="(item , index) in listaCorsi" :key="index" :corsi="item" class="corsiApp"></AppCorsi>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

header{
    font-family: 'Roboto', sans-serif; 
    width: 100%;
    .padding-container{
        
        .navbar{
        color: $colorGrey;
        font-size: 14px;

            select{
                color:$colorGrey;
                border: none;
            }

            .lista-icone{
                margin-left: 2rem;
            }
        }
    }
}

/* sezione dropdown category*/
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
    background-color: #fff;
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

/* sezione search bar*/
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

.container-icone{
    i{
        color:$colorLightblu;
    }
    span:hover{
        color:$colorLightblu;
        cursor: pointer;
    }
}

//sezione SIGN UP*/
.sign-up{
    color: $colorLightblu;

    .btn-sign-up{
        @include btn-red;
            &:hover{
                background-color: $colorLightblu;
            }
    }
    .fa-heart{
        font-size: 25px;
    }
}

.bk-blue{
    background-color: $colorBlue;
}

.container-small{
    max-width: 900px;
    margin: 0 auto;
}
.corsiApp{
    width: calc(100% / 5);
    padding: 30px 0px;
    color: #fff;

}
</style>