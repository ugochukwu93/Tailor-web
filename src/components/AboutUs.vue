<template>
  <div>
      <div class="about">
          <div class="about-flex">
            <div v-if="!mobile" class="about-box1"></div>
            <div class="about-box2"></div>
            <div class="about-box3"></div>
          </div>
          <div class="aboutme"  data-aos="fade-up" data-aos-duration="1000">
            <h2>About Us</h2>
            <p>We Aesthetic Design Hub, situated at Malad West, Mumbai, Maharashtra, provide great suits that fits you and your lifestyle. Our suits are made from the best quality fabrics and are guaranteed to give you durability and comfort. Our skilled master tailors handle all of our cutting and sewing, ensuring precision in all production processes and paying attention to the details. Unique styles that are a part of the current fashion trends and turn every woman into a fashionista. Our motto is to make all the women feel like a diva when they are dressed from head to toe in our eye catchy apparel.</p>
          </div>
          <img class="about-img" src="../assets/img/depositphotos_368291230-stock-photo-professional-tailor-african-american-woman.jpg" v-if="mobile"/>
          <img class="about-img2" src="../assets/img/serwaaamihere-4-removebg-preview.png" v-else/>
      </div>
      
  </div>
</template>

<script>
export default {
    data() {
        return {
            mobile: null,
        }
    },
    created() {
        this.checkScreen()
    },
    methods: {
        checkScreen() {
            const windowWidth = window.innerWidth;
            if (windowWidth <= 750) {
                this.mobile = true;
                return;
            }
            this.mobile = false
        }
    }

}
</script>

<style lang="scss" scoped>
.about {
    // display: flex;
    position: relative;
    @media(max-width: 600px) {
        display: block;
    }
    &-flex {
        display: flex;
        @media(max-width: 600px) {
            display: flex;
            height: 120%;
        }
    }

    &-box1 {
        background: #ffff;
        padding: 30px;
        height: 700px;
        width: 100%;

        
    }
    &-box2 {
        background: #433e49b9;
        padding: 30px;
        width: 100%;
        
        
    }
    &-box3 {
        background: #f3e8ebbb;
        padding: 30px;
        width: 100%;
        @media(max-width:600px) {
            height: 730px;
            
        }
       
    }
    &-img2 {
        position: absolute;
        top: 25px;
        left: 51rem;
        width: 470px;
        height: 650px;
    }
    &-img {
        width: 100%;
        height: 270px;
        padding: 0px 0px;
        position: absolute;
        top: 25px;
        
        
    }   

    

}   
.aboutme {
    position: absolute;
    top: 10rem;
    left: 7rem;
    text-align: center;
    background: rgba(255, 255, 255, 0.473);
    width: 600px;
    height: 400px;
    padding: 60px 20px;
    line-height: 30px;
    margin-bottom: 200px;
    @media(max-width: 600px) {
        padding: 60px 5px;
        position: absolute;
        top: 265px;
        width: 100%;
        height: 470px;
        left: 0;
    }
}
</style>