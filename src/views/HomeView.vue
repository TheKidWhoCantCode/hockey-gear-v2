<template>
  <Navbar :signedIn="signedIn" :userName="userName"/>

  <HomeContent></HomeContent>
  
  <div v-if="salesModal && !signedIn">
    <Modal @close="toggleModal('salesModal')" styleClass="newsletter">
      <div class="container">
        <div class="card">
          <h1>Be the first to know!</h1>
          <h2>Get Discounts!</h2>
          <p>Sign up now and get up to 20% off your first order!</p>
          <p><small>We don't share your email with any third party companies, promise!</small></p>
          <form action="#" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" novalidate>
            <input type="email" value="" name="EMAIL" class="email" id="mce-EMAIL" placeholder="Your email" required>
            <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="" tabindex="-1" value=""></div>
            <div class="clear"></div>
            <button name="subscribe" id="mc-embedded-subscribe" class="button" type="submit" @click.prevent="">Subscribe me</button>
          </form>
        </div>
      </div>
    </Modal>
  </div>

  <Footer></Footer>
  
</template>

<script>
import Navbar from '../components/Nav-bar.vue'
import Modal from '../components/Modal-template.vue'
import Footer from '../components/Footer-template.vue'
import HomeContent from '../components/Home-Content.vue'

export default {
  name: 'HomeView',
  components: {
    Navbar,
    Modal,
    Footer,
    HomeContent
  },
  data() {
    return {
      signedIn: false,
      userName: 'Username',
      salesModal: true
    }
  },
  methods: {
    toggleModal(modal) {
      this[modal] = !this[modal]
    },
    newsLetterSignUp() {
      //('.sign-up-container').addClass('submitted');
    }
  }
}

</script>

<style>
  
  body {
    margin: 0;
    background-color: rgb(255, 255, 255);
  }

  .container {
    top: 0%;
    margin: 0;
    display: flex;
    align-items: center;  
    flex-direction: column;
    height: 100vh;
    min-width: 300px;
  }

  .card {
    display: block;
    position: relative;
    width: 480px;
    max-width: 90%;
    min-height: 12em;
    background: #9d6ead;
    color: #ffffff;
    padding: 1em 2em 2em;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    text-align: center;
  }

  .card h1 { font-family: 'Dosis', sans-serif; font-weight: 400; font-size: 3rem; }

  .card form {
    display: flex;
    flex-flow: column wrap;
    align-items: center;
  }

  .card form input {
    display: flex;
    width: 80%;
  }

  .card form input.email {
    border: 0px;
    margin-bottom: 1em;
    padding: .3em 1em;
    text-align: center;
    font-family: monospace;
    font-size: 24px;
    line-height: 30px;
    outline: none !important;
    border-radius: 5px;
    background-color: #F1FFFA;
  }

  .card form button {
    border: 0px transparent;
    padding: 1em 1.2em;
    border-radius: 5px;
    background-color: #2544b1;
    color: #ffffff;
    font-family: 'Source Sans Pro', sans-serif;
    font-size: 18px;
    letter-spacing: 0;
    font-weight: 700;
    text-transform: uppercase;
    transition: .4s all ease-in-out;
    cursor: pointer;
  }

  .card form button:hover { background-color: #F17C73; }

</style>
