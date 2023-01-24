<script>
export default {
    props:{
        icone:Object
    }
}
</script>
<template lang="">
        <i :class="icone.label"></i>
</template>

<style lang="scss" scoped>
    
    @use '../../assets/style/partials/mixin' as *;
    @use '../../assets/style/partials/variables' as *;

i{
    margin: 0px 5px;
    &:hover{
        color: $colorLightblu;
        cursor: pointer;
    }
}

</style>