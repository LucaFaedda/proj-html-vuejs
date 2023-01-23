<script>
export default {
    props:{
        icone:Object
    }
}
</script>
<template lang="">
    <div>
        <li class="mx-1">
            <i :class="icone.label">
                
            </i>
        </li>
    </div>
</template>

<style lang="scss" scoped>
    
@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

</style>