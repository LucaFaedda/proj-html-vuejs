<script>
    export default {

        props:{
            categoria: Object
        }
    }
</script>
<template lang="">
        <li>
            <a>
                {{categoria.label}}
            </a>
        </li>
</template>
<style lang="scss" scoped>
    
@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

li {
    width: 250px;
    border-bottom: 1px solid #fff;
}

li a {
    display: block;
    padding: 7px;
    text-decoration: none;
}


</style>