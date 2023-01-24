<script>
  export default {
      
  }
</script>
<template lang="">
  <footer class="container-fluid">
    <div class="container-small">
      <div class="row">
        <div class="col-3">
          <h2>about</h2>

        </div>
        <div class="col-3">
          <h2>contact</h2>
          
        </div>
        <div class="col-3">
          <h2>social network</h2>
        </div>
        <div class="col-3">
          
        </div>

      </div>
                
    </div>
  </footer>
</template>
<style lang="scss" scoped>

@use '../assets/style/partials/mixin' as *;
@use '../assets/style/partials/variables' as *;

footer{
  background-color: $colorBlue;

    .container-small{
      max-width: 1176px;
      margin: 0 auto;

        h2{
          color: #fff;
          font-weight: bold;
        }
    }
}
  
</style>