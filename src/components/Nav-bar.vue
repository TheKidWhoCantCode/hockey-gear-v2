<template>
    <div class="nav">
        <table>
            <tr>
                <td>
                    <div class="logoContainer">
                        <svg>
                            <text id="logo" x="50%" y="40%" text-anchor="middle" fill="none">Hockey Gear</text>
                            <use xlink:href="#logo" class="copy copy1"></use>
                            <use xlink:href="#logo" class="copy copy2"></use>
                            <use xlink:href="#logo" class="copy copy3"></use>
                            <use xlink:href="#logo" class="copy copy4"></use>
                            <use xlink:href="#logo" class="copy copy5"></use>
                        </svg>
                    </div>
                </td>

                <td><router-link to="/">Home</router-link></td>
                <td><router-link to="/products">Products</router-link></td>
                <td><router-link to="/about">About</router-link></td>
                <td><router-link to="/contact">Contact</router-link></td>
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
        height: 20%;
        margin: 0;
        font-size: 20px;
        font-weight: 500;
        font-style: normal;
        text-decoration: none;
        color: black;
        padding: 0px;
        background-color: white;
        box-shadow: 0px 0px 10px 1px black;
    }
    table h2 {
        font-weight: 500;
    }
    table a {
        color: black;
        text-decoration: none;
    }
    img {
        margin-right: 15px;
        width: 20px;
    }
    .logoContainer {
        height: 10vh;
    }
    #logo {
        font-size: 50px;
    }
    .copy {
        fill: none;
        stroke: #db902d;
        stroke-width: 2px;
        stroke-dasharray: 8% 30%;
        stroke-dashoffset: 0%;
        animation: logoAnimation 10s linear infinite;
    }
    @keyframes logoAnimation {
        50% {
            stroke-dashoffset: -35%;
        }
        100% {
            stroke-dashoffset: 0%;
        }
    }
    .copy1 {
        stroke: rgb(70, 199, 199);
        animation-delay: -1s;
    }
    .copy2 {
        stroke: rgb(175, 16, 56);
        animation-delay: -2s;
    }
    .copy3 {
        stroke: rgb(215, 144, 236);
        animation-delay: -3s;
    }
    .copy4 {
        stroke: rgb(122, 156, 140);
        animation-delay: -4s;
    }
</style>