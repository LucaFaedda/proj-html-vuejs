<script>

export default {
    props:{
        navbar:Object
    },

}
</script>
<template lang="">
    <li class="mx-2">
        <a class="dropdown">
            <a  href="#"  data-bs-toggle="dropdown" aria-expanded="false">
                {{ navbar.label}}
            </a>
            <ul class="dropdown-menu " >
                <li>
                    <a class="dropdown-item " href="#" v-for="item in navbar.children">
                        {{ item.label_2}}
                        <!-- <ul class="dropdown-menu dropdown-submenu">
                            <li>
                                <a class="dropdown-item" href="#" v-for="item in navbar.children.children_2">
                                    {{item.label_3}}
                                </a>
                            </li>
                        </ul> -->
                    </a>
                </li>
            </ul>
        </a>
        <!-- ciclare di nuovo l'array sennò ovviamente non trova nulla -->
    </li>
    
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;



</style>