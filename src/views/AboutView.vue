<template>
  <Navbar></Navbar>

  <div class="container">
    <h1>About us!</h1>
    <p>Welcome to Hockey Gear, your premier destination for high-quality field hockey sticks. Founded by passionate field hockey players, we understand the importance of having the right gear to excel in this dynamic sport.</p>
    <h2>Our Story</h2>
    <p>Our journey began on the field, where we shared the same love and dedication for field hockey. Frustrated by the lack of options for quality field hockey sticks, we decided to take matters into our own hands and create a brand that players could trust. Thus, Hockey Gear was born.</p>
    <h2>Our Mission</h2>
    <p>At Hockey Gear, our mission is simple: to provide field hockey players of all levels with the best equipment possible. We believe that having the right stick can make a world of difference in your game. That's why we are committed to delivering top-notch products that meet the highest standards of performance, durability, and design.</p>
    <h2>Why Choose us?</h2>
    <ol>
      <li><b>Expertise:</b> We're not just a company; we're field hockey enthusiasts with years of experience. Our team is dedicated to staying up-to-date with the latest innovations in stick technology to ensure we offer the best options available.</li>
      <li><b>Quality Assurance:</b> Every field hockey stick we offer has been rigorously tested and chosen for its superior quality. We only sell products we would use ourselves, so you can trust that you're getting the best.</li>
      <li><b>Variety:</b> We understand that every player is unique. That's why we offer a wide range of field hockey sticks to cater to different playing styles, skill levels, and preferences.</li>
      <li><b>Customer Satisfaction:</b> Your satisfaction is our top priority. We pride ourselves on providing exceptional customer service, from helping you choose the right stick to assisting with any post-purchase questions or concerns.</li>        <li><b>Community:</b> We're not just a store; we're a part of the field hockey community. We actively support local teams, events, and initiatives to help grow and strengthen the sport we love.</li>
    </ol>
    <h2>Join Us in the Game</h2>
    <p>Whether you're a seasoned professional or just starting your field hockey journey, we invite you to explore our collection of field hockey sticks and gear. We're here to equip you with the tools you need to perform at your best and enjoy every moment on the field.</p>
    <p>Thank you for choosing Hockey Gear as your trusted partner in field hockey. We look forward to being a part of your success on the field!</p>
  </div>
  
  <Footer></Footer>
</template>

<script>
import Navbar from '../components/Nav-bar.vue'
import Footer from '../components/Footer-template.vue'

export default {
    name: 'aboutview',
    components: { Navbar, Footer }
}
</script>

<style scoped>
  .container {
    margin: 500px;
    margin-top: 10px;
    margin-bottom: 100px;
  }
  ol {
    text-align: left;
    margin-left: 100px;
  }
  h2 {
    margin-top: 30px;
  }
</style>