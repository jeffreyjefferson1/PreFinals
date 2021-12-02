<template>
    
 <div class="row">
        <div class="col-md-4">
             <div class="card card-deck">
                    <div class="card text-white bg-success mb-3 " style="width: 18rem">
                        <img class="card-img-top imgs p-3" :src="product.img" alt="Card image cap" />
                        <div class="card-body">
                            <h3 class="card-title">{{ product.name }}</h3>
                            Price: ${{ product.price }}.00
                            <br>
                        </div>
                        <div class="card-footer bg-grey">
                            <div class="d-grid gap-2">
                                <button type="button" class="btn btn-lg btn-light text-dark btn-outline-secondary" 
                                @click="$emit('viewProd', product)">Show</button>
                            </div>
                    </div>
            </div>
        </div>
        </div>
    </div>
    
</template>

<script>
    export default {
        props: ['product'],
            // img() {
            //     return this.product.img;
            // }
    }
</script>

<style>
.imgs{
    height: 200px !important;
    width: auto !important;
}
.card-deck{
    margin: 10px 10px ;
    background-color: rgb(255, 255, 255);
}
.card{
    padding:3px !important;
}

</style>