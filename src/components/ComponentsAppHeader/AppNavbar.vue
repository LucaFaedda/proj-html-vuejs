<script>

export default {
    props:{
        navbar:Object
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
    <div class="mx-3" >
        <a v-if="!navbar.children">
            {{ navbar.label}} 
        </a>
        <span v-else v-on:mouseover="onOver" v-on:mouseleave="onLeave" class="contenitore-dropdown ms-1">
            {{ navbar.label}} 
            <ul class="menu-discesa"  :class="{ isOpen }" >
                <li>
                    <a  href="#" v-for="item in navbar.children">
                        {{ item.label_2}}
                       
                    </a>
                </li>
            </ul>
        
        </span>

        <!-- ciclare di nuovo l'array sennò ovviamente non trova nulla -->
    </div>
    
</template>
<style lang="scss" scoped>

@use '../../assets/style/partials/mixin' as *;
@use '../../assets/style/partials/variables' as *;

a{
    color:$colorGrey;
    cursor: pointer;
}

.contenitore-dropdown{
    position: relative;
}

.menu-discesa{
    position: absolute;
    top: 100%;
    left: 0;
    
    display: none;
    padding: 10px 50px 10px 0px;
    width: 200px;
    list-style-type: none;
    background-color: #ffff;
    text-align: left;
    border-top: 2px solid $colorRed;
    box-shadow: 5px 5px 10px 0px #535252;
}

.isOpen {
    display: block;
}

li a {
    display: block;
    padding: 7px;
    text-decoration: none;
    color: #000;
}




</style>