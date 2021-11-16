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
          <div>
              <img src="../assets/img/email.png" />
              <h3>Our Office Address</h3>
              <span>contact@gmail.com</span>
          </div>
          <div>
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

}
</script>

<style lang="scss" scoped>
h2 {
    text-align: center;
    margin-top: 50px;
}
.contact {
    display: flex;
    justify-content: space-around;
    margin: 90px 0px 100px 90px;
    // justify-content: center;
    img {
        width: 35px;
        margin-bottom: 30px;
    }
    div {
        text-align: center;
        padding: 40px 100px 40px 40px;
        border-right: 2px solid rgb(236, 233, 233);

        span {
            opacity: 0.5;
        }
    }
}
</style>