<template>
    <img src="../assets/Mercian.jpg">
    
    <div class="productContainer">
        <ProductCard productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="../assets/Mercian_CKF_95_ProductImage"></ProductCard>
        <ProductCard productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="../assets/Mercian_CKF_95_ProductImage"></ProductCard>
        <ProductCard productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="../assets/Mercian_CKF_95_ProductImage"></ProductCard>
        <ProductCard productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="../assets/Mercian_CKF_95_ProductImage"></ProductCard>
        <ProductCard productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="../assets/Mercian_CKF_95_ProductImage"></ProductCard>
        <ProductCard productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="../assets/Mercian_CKF_95_ProductImage"></ProductCard>
    </div>

</template>

<script>
import ProductCard from "./Product-Card.vue"

export default {
    components: {
        ProductCard
    }
}
</script>

<style scoped>
    img {
        height: 600px;
        width: 100%;
    }

    .productContainer {
        display: grid;
        grid-template-columns: auto auto auto;
    }
</style>