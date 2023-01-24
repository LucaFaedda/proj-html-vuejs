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
        <a href="#" >{{corsi.label}}</a>
        <ul class="menu-discesa"  :class="{ isOpen }" >
            <li class="d-flex justify-space-between">
                <a  href="#" v-for="item in corsi.children" class="d-flex">
                    <i :class="item.icons_2" class="icone-hover"></i>
                    <span class="mx-2">{{ item.label_2}}</span>
                       
                </a>
            </li>
        </ul>

    </div>
    
</template>

<style lang="scss" scoped>
@use '../../assets/style/partials/mixin' as *;
@use '../../assets/style/partials/variables' as *;

.corsi{

    position: relative;
    text-align: center;
    color: #fff;
    i{
        font-size: 20px;
    }
    
    a{
        font-size: 16px;
        color: #fff;
        
    }

    &:hover{
        background-color: $colorLightblu;
        cursor: pointer;
    }

}
    .menu-discesa{
    position: absolute;
    top: 100%;
    left: 0px;
    display: none;
    padding: 40px 30px;
    width: auto;
    list-style-type: none;
    background-color: $colorLightblu;
    text-align: left;
    font-size: 14px;

}

.isOpen {
    display: block;
}

li a {
    display: block;
    padding: 7px;
    text-decoration: none;
    color:#fff;
}

.icone-hover:hover{
    margin-right: 5px;
}

</style>