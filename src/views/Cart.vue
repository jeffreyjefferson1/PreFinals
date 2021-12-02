<template>
    <div>
        <h1 class="text-white mb-5 fw-bold bg-secondary">CART:</h1>

        <!-- <div v-for="product in items" :key="product.id">
            {{ product.name }}
        </div> -->

        <CartItemCard 
           v-for="product in products"
           :key="product.id"
           :product="product" />

        
    </div>
</template>

<script>
import CartItemCard from '../components/cart/CartItemCard.vue'

    export default {
        components: {
            CartItemCard
        },
        computed: {
            products() {
                return this.$store.getters.cartItems
            }
        }
    }
</script>
