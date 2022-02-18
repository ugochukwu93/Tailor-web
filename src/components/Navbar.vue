<template>
  <div>
      <div class="navbar">
          <BookModal
          v-if="modal"
          />
        <div class="navbar-social" style="">
            <img src="../assets/img/facebook.png" @click="openLink('https://www.facebook.com/African-Fashion-119072299631574/')" width="20"/>
            <img src="../assets/img/instagram.png" @click="openLink('https://www.instagram.com/fashionafricana/')" width="20"/>
            <img src="../assets/img/twitter.png" @click="openLink('https://www.facebook.com/African-Fashion-119072299631574/')" width="20"/>
            <img src="../assets/img/pinterest.png" @click="openLink('https://www.facebook.com/African-Fashion-119072299631574/')" width="20"/>
        </div>
        <div class="navbar-link">
          <img src="../assets/img/sewing-machine.png" width="40">
          <span> <a href="#home">Home</a></span>
          <span> <a href="#pricing">Pricing</a></span>
          <span><a href="#categories">Categories</a></span>
          <span><a href="#services">Services</a></span>
          <span @click="openLink('https://www.instagram.com/fashionafricana/')">Catalogue</span>
          <span> <a href="#contact">Contact</a></span>
          <!-- <span @click="modal=true">Book Online</span> -->
        </div>
      </div>
  </div>
</template>

<script>
import BookModal from './BookModal.vue'
export default {
    components: {
        BookModal,
    },
    data() {
        return {
            modal: false,
        }
    },
methods: {
    openLink(url) {
      const win = window.open(url, "_blank");
      win.focus();
    },
    openModal() {
        this.modal == false
    }
}
}
</script>

<style lang="scss" scoped>
.navbar {
    position: fixed;
    top: 0px;
    z-index: 8000;
    transition: top 0.3s;
    background: #ffffff;
    transform: translate3d(0, 0, 0);
    height: 100px;
    // display: flex;
    align-items: center;
    // padding-left: 40px;
    // padding-right: 40px;
    width: 100%;
    box-shadow: 0px 3px 6px #00000029;
    // 
    &-link {
        padding-left: 50%;
        padding-top: 25px;
        display: flex;
        position: relative;

        img {
            position: absolute;
            top: 15px;
            left: 100px;
        }
    }
    &-social {
        height: 30px;
        padding: 5px 0px 5px 20px;
        background: #F3E8EB;
        img {
            margin-left: 30px;
            cursor: pointer;
        }
    }
    span {
        margin-left: 50px;
        color:#433E49;
        font-weight: bold;
        cursor: pointer;
        a {
            text-decoration: none;
            color:#433E49;
        }

    }
}
</style>>