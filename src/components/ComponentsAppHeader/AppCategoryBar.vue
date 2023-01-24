<script>
    export default {

        props:{
            categoria: Object
        }
    }
</script>
<template lang="">
        <a>
            {{categoria.label}}
        </a>
</template>
<style lang="scss" scoped>
    
    @use '../../assets/style/partials/mixin' as *;
    @use '../../assets/style/partials/variables' as *;


a {
    display: block;
    padding: 7px;
    text-decoration: none;
    width: 250px;
    border-bottom: 1px solid #fff;
}


</style>