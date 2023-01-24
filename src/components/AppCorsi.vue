<script>
export default {
    props:{
        corsi:Object
    }
}
</script>
<template lang="">
    <div class="corsi">
        <i :class="corsi.icons" class="me-3"></i>
        <a href="#">{{corsi.label}}</a>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

.corsi{
    i{
        font-size: 20px;
    }
    
    a{
        color: #fff;
        font-size: 16px;
    }

}
    
</style>