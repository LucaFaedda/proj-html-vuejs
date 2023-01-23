<script>

export default {
    props:{
        navbar:Object
    }
}
</script>
<template lang="">
    <li>
        <a class="dropdown">
            <a  href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                {{ navbar.label}}
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>

        </a>


    </li>
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;


</style>