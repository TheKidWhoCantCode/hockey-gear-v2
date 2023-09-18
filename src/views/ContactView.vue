<template>
    <Navbar></Navbar>

    <div class="formContainer">
        <form>
            <h1>Send a meassage</h1>
            <label for="name">Name</label>
            <input type="text" id="name" name="name">
            <br>
            <label for="email">Email</label>
            <input type="email" id="email" name="email">
            <br>
            <label for="message">Message</label>
            <br>
            <textarea maxlength="400"></textarea>
            <br>
            <button @click.prevent>Send!</button>
        </form>
    </div>

    <Footer style="position: absolute; bottom: 0%; width: 100%;"></Footer>
</template>

<script>
import Navbar from '../components/Nav-bar.vue'
import Footer from '../components/Footer-template.vue'

export default {
    name: 'aboutView',
    components: { Navbar, Footer }
}
</script>

<style scoped>

h1 {
    font-weight: 900;
    color: white;
}

label {
    margin: 10px;
    font-weight: bold;
    color: rgb(255, 255, 255);
}
input {
    margin: 10px;
    border: none;
    border-radius: 3px;
}

button {
    margin-top: 2vh;
    width: 20vh;
    height: 3vh;
}
.formContainer {
    width: 50%;
    height: 50%;

    background-color: rgb(221, 163, 88);
    border-radius: 10px;
    box-shadow: 5px 5px 30px 1px;

    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
textarea {
    position: relative;
    resize: none;
    height: 20vh;
    width: 30vh;
    border-radius: 5px;
}
</style>