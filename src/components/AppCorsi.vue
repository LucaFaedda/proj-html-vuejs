<script>
export default {
    props:{
        corsi:Object
    },
    data(){
        return{
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
    <div class="corsi" v-on:mouseover="onOver" v-on:mouseleave="onLeave">
        <i :class="corsi.icons" class="me-3"></i>
        <a href="#">{{corsi.label}}</a>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

.corsi{

    text-align: center;
    i{
        font-size: 20px;
    }
    
    a{
        color: #fff;
        font-size: 16px;
    }

    &:hover{
        background-color: $colorLightblu;
        cursor: pointer;
    }

}
    
</style>