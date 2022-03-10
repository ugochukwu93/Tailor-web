<template>

  <div id="contact">
      <div>
          <h2>Contact Us</h2>
      </div>
      <div class="contact">
          <div>
              <img src="../assets/img/location.png"/>
              <h3>Our Office Address</h3>
              <span>No 62, Seaside Road <br> Port harcourt Rivers State</span>
          </div>
          <div @click="openLink('mailto:nwadikeugochukwu93@gmail.com')" class="mail">
              <img src="../assets/img/email.png" />
              <h3>Our Office Address</h3>
              <span>contact@gmail.com</span>
          </div>
          <div @click="openLink('https://wa.me/+23407062479020?text=Hi%20There!')" class="watsApp">
              <img src="../assets/img/call.png" />
              <h3>Call Us / Whats App</h3>
              <span>+234905673575</span>
          </div>
          <div style="border: none;">
              <img src="../assets/img/clock.png"/>
              <h3>Our Timing</h3>
              <span>Mon-Sun: 09:00 AM-09:00 PM</span>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    methods: {
    openLink(url) {
      const win = window.open(url, "_blank");
      win.focus();
    },
    
}
}
</script>

<style lang="scss" scoped>
h2 {
    text-align: center;
    margin-top: 50px;
    @media(max-width: 600px) {
        margin-top: 30px;
    }
}
.contact {
    display: flex;
    justify-content: space-around;
    margin: 90px 0px 100px 90px;
    // justify-content: center;
    @media(max-width: 600px) {
        display: block;
        margin: 40px 0px 50px 90px;
    }
    
    img {
        width: 35px;
        margin-bottom: 30px;
        @media(max-width: 600px) {
             margin-bottom: 10px;
        }
    }
    div {
        text-align: center;
        padding: 40px 100px 40px 40px;
        border-right: 2px solid rgb(236, 233, 233);
        @media(max-width: 600px) {
            border-right: none;
            padding: 5px 120px 10px 40px;
        }

        span {
            opacity: 0.5;
        }
    }
}
.watsApp {
    cursor: pointer;
}
.mail {
    cursor: pointer;
}
</style>