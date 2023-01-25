<script>
    export default {
            props:{
                cardpopolari: Object
            }
    }
</script>
<template lang="">

    <div class="card" style="width: 17rem;" >
        <img src="../assets/img/`${cardpopolari.img}`" class="card-img-top" alt="apple-products">
        <div class="card-body">
                <p class="card-title">{{cardpopolari.cardTitle}}</p>
                <p class="card-text">{{cardpopolari.cardText}}</p>
                <hr>
            <div class="d-flex justify-content-between">
                    <div>
                        <img src="../assets/img/starfull.svg">
                        <img src="../assets/img/starfull.svg">
                        <img src="../assets/img/starfull.svg">
                        <img src="../assets/img/starfull.svg">
                        <img src="../assets/img/staremptyl.svg">
                    </div>

                <p class="m-0 old-price">{{cardpopolari.OldPrice}}</p>
                <h6 >{{cardpopolari.price}}</h6>
            </div>
        </div>
    </div>

</template>
<style lang="">
    
</style>