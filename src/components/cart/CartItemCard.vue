<template>

    <div class="align-item-center cart-item-card card mb-3 bg-light text-dark border border-outline-secondary" style="width: 10rem;">
        <div class="card-header">
            <h3> {{ product.name }} </h3>
        </div>
        <ul class="list-group list-group-flush border border-outline-secondary">
            <li class="list-group-item bg-success text-white border border-outline-secondary">In Cart: {{ product.quantity }}</li>
            <li class="list-group-item bg-success text-white border border-outline-secondary">Total Cost: {{ item_cost.toFixed(2) }}</li>
        </ul>
    </div>


    
</template>

<script>
    export default {
        props: ['product'],
        computed: {
            description() {
                return this.product.description.substring(0, 100)
            },
            item_cost() {
                return this.product.price * this.product.quantity;
            }
        }
    }
</script>


<style>
    .card {
        margin: 0 auto; 
        float: none; 
        margin-bottom: 10px; 
        text-align: left;
}

</style>