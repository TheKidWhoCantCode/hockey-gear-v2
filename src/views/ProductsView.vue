<template>
    <NavBar></NavBar>
      
    <div class="searchBar">
        <input type="text" id="searchInput" onkeyup="search()" placeholder="Search..." title="Type in a category">
    </div>

    <div class="colourBar"></div>

    <div class="productsContainer">
        <div class="row">
            <ProductCard style="float: left; margin-left: 200px;" productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="Mercian_CKF_95_ProductImage.png"></ProductCard>
            <ProductCard style="float: left;" productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="Mercian_CKF_95_ProductImage.png"></ProductCard>
        </div>

        <div class="row">
            <ProductCard style="float: left; margin-left: 200px;" productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="Mercian_CKF_95_ProductImage.png"></ProductCard>
            <ProductCard style="float: left;" productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="Mercian_CKF_95_ProductImage.png"></ProductCard>
        </div>

        <div class="row">
            <ProductCard style="float: left; margin-left: 200px;" productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="Mercian_CKF_95_ProductImage.png"></ProductCard>
            <ProductCard style="float: left;" productName="Mercian CKF 95" productCopy="Very good hockey stick" price="200" productImageSrc="Mercian_CKF_95_ProductImage.png"></ProductCard>
        </div>
    </div>

    <div class="filterBar">
        <h2>Filters</h2>

        <!-- Price SELECT -->
        <h3>Max price</h3>
        <form style="text-align: center; margin: 0;">
            <input type="text" id="maxPrice" value="6000">
        </form>
        <br>

        <!-- BOW SELECT -->
        <h3>Select Bow</h3>
        <form>
            <input type="checkbox" id="midBow" name="bow" value="Mid Bow">
            <label for="midBow">Mid Bow</label><br>

            <input type="checkbox" id="lowBow" name="bow" value="Low Bow">
            <label for="lowBox">Low Bow</label><br>

            <input type="checkbox" id="elBow" name="bow" value="Extreme Low Bow">
            <label for="elBow">Extreme Low Bow</label><br>
        </form>
        <br>

        <!-- Colour SELECT -->
        <h3>Select Colour</h3>
        <form>
            <input type="checkbox" id="black" name="colour" value="black">
            <label for="black">Black</label><br>

            <input type="checkbox" id="blue" name="colour" value="blue">
            <label for="blue">Blue</label><br>
            
            <input type="checkbox" id="yellow" name="colour" value="yellow">
            <label for="yellow">yellowellow</label><br>

            <input type="checkbox" id="white" name="colour" value="white">
            <label for="white">White</label><br>

            <input type="checkbox" id="gray" name="colour" value="gray">
            <label for="gray">Gray</label><br>
        </form>
        <br>

        <!-- Brand SELECT -->
        <h3>Select Brand</h3>
        <form>
            <input type="checkbox" id="adidas" name="brand" value="adidas">
            <label for="adidas">Adidas</label><br>

            <input type="checkbox" id="gryphon" name="brand" value="gryphon">
            <label for="gryphon">Gryphon</label><br>
            
            <input type="checkbox" id="mercian" name="brand" value="mercian">
            <label for="mercian">Mercian</label><br>

            <input type="checkbox" id="osaka" name="brand" value="osaka">
            <label for="osaka">Osaka</label><br>

            <input type="checkbox" id="jdh" name="brand" value="jdh">
            <label for="jdh">JDH</label><br>
            
            <input type="checkbox" id="y1" name="brand" value="y1">
            <label for="y1">Y1</label><br>
        </form>
        <br>
    </div>

    <Footer style="width: 80%; margin-left: 20%;"></Footer>
</template>

<script>
import NavBar from '../components/Nav-bar.vue'
import Footer from '../components/Footer-template.vue'
import ProductCard from '../components/Product-Card.vue';
import { isRuntimeOnly } from 'vue';

export default {
    name: 'ProductsView',
    components: {
        Footer,
        NavBar,
        isRuntimeOnly,
        ProductCard
    },
    methods: {
    }
}

</script>

<style>
    .filterBar {
        border-right: 1px solid black;
        height: 25px;
        background-color: rgb(233, 233, 233);
        position: fixed;
        bottom: 0; 
        width: 20%; 
        height: 80%;
    }
    form {
        text-align: left; 
        margin-left: 80px;
    }
    .productsContainer {
        margin-top: 100px;
        margin-left: 20%;
        width: 80%;
        height: 1000px;
    }
    .row:after {
        content: "";
        display: table;
        clear: both;
    }
    .searchBar {
        background-color: rgb(48, 22, 48);
        height: 98px;
    }
    #searchInput {
        width: 50%;
        float: right;
        margin-top: 25px;
        font-size: 18px;
        padding: 11px;
        border: 1px solid #ddd;
    }
    .colourBar {
        width: 20.02%;
        height: 423px;
        border-right: 1px solid black;
        float: left;
        background-color: rgb(233, 233, 233);
    }

</style>