<template>
  <div>
      <div class="about">
          <div class="about-box1"></div>
          <div class="about-box2"></div>
          <div class="about-box3"></div>
          <div class="aboutme"  data-aos="fade-up" data-aos-duration="1000">
            <h2>About Us</h2>
            <p>We Aesthetic Design Hub, situated at Malad West, Mumbai, Maharashtra, provide great suits that fits you and your lifestyle. Our suits are made from the best quality fabrics and are guaranteed to give you durability and comfort. Our skilled master tailors handle all of our cutting and sewing, ensuring precision in all production processes and paying attention to the details. Unique styles that are a part of the current fashion trends and turn every woman into a fashionista. Our motto is to make all the women feel like a diva when they are dressed from head to toe in our eye catchy apparel.</p>
          </div>
          <img src="../assets/img/serwaaamihere-4-removebg-preview.png"/>
      </div>
      
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.about {
    display: flex;
    position: relative;

    &-box1 {
        background: #ffff;
        padding: 30px;
        width: 100%;
        height: 700px;
        
    }
    &-box2 {
        background: #433E49;
        padding: 30px;
        width: 100%;
        
    }
    &-box3 {
        background: #F3E8EB;
        padding: 30px;
        width: 100%;
       
    }
    img {
        position: absolute;
        top: 25px;
        left: 51rem;
        width: 470px;
        height: 650px;
    }
}
.aboutme {
    position: absolute;
    top: 10rem;
    left: 7rem;
    text-align: center;
    background: #ffff;
    width: 600px;
    height: 400px;
    padding: 60px 20px;
    line-height: 30px;
}
</style>