<template>
    <div class="nav">
        <table>
            <tr>
                <td><h2>Hockey Gear</h2></td>
                <td><router-link to="/">Home</router-link></td>
                <td><router-link to="/products">Products</router-link></td>
                <td><router-link to="/about">About</router-link></td>
                <td><router-link to="/contact">contact</router-link></td>
                <td v-if="!signedIn">Sign In / Sign Up</td>
                <td v-if="signedIn">Hello, {{ userName }}!</td>
                <td><router-link to="/cart"><img src="../assets/cart-ico.png">Cart</router-link></td>
            </tr>
    </table>
    </div>
</template>

<script>
export default {
    props: [ 'signedIn', 'userName' ],
    methods: {

    }
}

</script>

<style>
    table {
        width: 100%;
        height: 20px;
        margin: 0;
        font-size: 20px;
        font-weight: 500;
        padding: 0px;
        background-color: white;
        box-shadow: 0px 0px 10px 1px black;
    }
    table h2 {
        font-weight: 500;
    }
    img {
        margin-right: 15px;
        width: 20px;
    }
</style>