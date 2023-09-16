<template>
    <div class="card">
    <div class="column">
        <h2>{{ productName }}</h2>
        <p class="price">${{ price }}</p>
        <p>{{ productCopy }}</p>
        <p><button>Add to Cart</button></p>
    </div>
    <div class="column">
        <img :src="productImageSrc" style="width:100%">
    </div>
</div>
</template>

<script>
export default {
    props: ['productName', 'productCopy', 'price', 'productImageSrc']
}
</script>

<style scoped>
    .card {
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        background-color: white;
        max-width: 600px;
        margin: 10px;
        text-align: center;
        font-family: arial;
    }
    .card:after {
        content: "";
        display: table;
        clear: both;
    }
    
    .price {
        color: grey;
        font-size: 22px;
    }

    .card button {
        border: none;
        outline: 0;
        padding: 12px;
        color: white;
        background-color: #000;
        text-align: center;
        cursor: pointer;
        width: 100%;
        font-size: 18px;
    }

    .card button:hover {
          opacity: 0.7;
    }
    p, h2{
        color: black;
    }
    .column {
        float: left;
        width: 45%;
        padding: 10px;
    }
</style>