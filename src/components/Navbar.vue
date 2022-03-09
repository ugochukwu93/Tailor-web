<template>
  <div>
      <div class="nav"
      :class="{ 'hidden-navbar': !showHeader }">
          <BookModal 
          v-show="isModalVisible" 
          @close="closeModal"
         />
        <div class="nav-social" style="" v-if="!mobileView">
            <img src="../assets/img/facebook.png" @click="openLink('https://www.facebook.com/African-Fashion-119072299631574/')" width="20"/>
            <img src="../assets/img/instagram.png" @click="openLink('https://www.instagram.com/fashionafricana/')" width="20"/>
            <img src="../assets/img/twitter.png" @click="openLink('https://www.facebook.com/African-Fashion-119072299631574/')" width="20"/>
            <img src="../assets/img/pinterest.png" @click="openLink('https://www.facebook.com/African-Fashion-119072299631574/')" width="20"/>
        </div>
        <div class="nav-link" v-if="!mobileView">
          <img src="../assets/img/sewing-machine.png" width="40">
          <span> <a href="#home">Home</a></span>
          <span> <a href="#pricing">Pricing</a></span>
          <span><a href="#categories">Categories</a></span>
          <span><a href="#services">Services</a></span>
          <span @click="openLink('https://www.instagram.com/fashionafricana/')">Catalogue</span>
          <span> <a href="#contact">Contact</a></span>
          <span @click="showModal">Book Online</span>
        </div>
        <header class="header" v-if="mobileView">
    <nav class="header__nav">
        <img src="../assets/img/sewing-machine.png" width="50">
      <ul class="header__navbar">
        <li class="header__item" style="list-style-type: none;">
          <a href="#" class="header__link">
            <transition name="slide-fade">
              <!-- Header Navigation Menu Icons -->
              <button class="header--button" v-if="show" key="on" @click="show = false">
                <img src="../assets/img/close.png" width="40"/>
              </button>
              <button class="header--button" v-else key="off" @click="show = true">
                <img src="../assets/img/menu.png" width="60"/>
              </button>
            </transition>
          </a>
          <!-- Dropdown Menu -->
          <transition name="dropdown">
            <div class="dropdown__menu" v-bind:class="{ active: show }" v-if="show">
              <ul class="dropdown__menu-nav">
                <div> <a href="#home">Home</a></div>
                <div> <a href="#pricing">Pricing</a></div>
                <div><a href="#categories">Categories</a></div>
                <div><a href="#services">Services</a></div>
                <div @click="openLink('https://www.instagram.com/fashionafricana/')">Catalogue</div>
                <div> <a href="#contact">Contact</a></div>
                <div @click="showModal">Book Online</div>
              </ul>
            </div>
          </transition>
        </li>
      </ul>
    </nav>
  </header>
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
        isModalVisible: false,
        showHeader: true,
        lastScrollPosition: 0,
        scrollOffset: 40,
        show: false,
        mobileView: null,
    }
},
created() {
    this.checkScreen();
    window.addEventListener("resize", this.checkScreen);
},
beforeDestroy() {
    window.removeEventListener('scroll', this.onScroll)
},
mounted() {
    this.lastScrollPosition = window.pageYOffset
    window.addEventListener('scroll', this.onScroll)
},
methods: {
    openLink(url) {
      const win = window.open(url, "_blank");
      win.focus();
    },
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    },
    onScroll() {
    if (window.pageYOffset < 0) {
      return
    }
    if (Math.abs(window.pageYOffset - this.lastScrollPosition) < this.scrollOffset) {
      return
    }
    this.showHeader = window.pageYOffset < this.lastScrollPosition
    this.lastScrollPosition = window.pageYOffset
  },
  checkScreen() {
      const windowWIdth = window.innerWidth;
      if (windowWIdth <= 720) {
        this.mobileView = true;
        return;
      }
      this.mobileView = false;
    },
}
}
</script>

<style lang="scss" scoped>
.nav {
    position: fixed;
    top: 0px;
    z-index: 8000;
    transition: top 0.3s;
    background: #ffffff;
    transform: translate3d(0, 0, 0);
    height: 100px;
    // display: flex;
    align-items: center;
    min-width: 100%;
    box-shadow: 0px 3px 6px #00000029;
    @media (max-width:600px) {
        position: absolute;
        top: 0px;
        // z-index: 8000;
        transition: top 0.3s;
        background: #ffffff7e;
        transform: translate3d(0, 0, 0);
        height: 80px;
        box-shadow: 0px 3px 6px #00000029;
            // width: 10%;
            // width: 10%;
            // height: 12.51px;
        }
        // 
    &-link {
        padding-left: 42%;
        padding-top: 25px;
        display: flex;
        position: relative;
        @media (max-width:600px) {
            padding-left: 5%;
        min-width: 1%;
        display: inline-block;
        // width: 10%;
        // height: 12.51px;
    }

        img {
            position: absolute;
            top: 15px;
            left: 100px;
        }
    }
    &-social {
        height: 30px;
        width: 100%;
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
.hidden-navbar {
  box-shadow: none;
  transform: translateY(-100%);
  transition: transform 300ms linear;
}
@media only screen and (max-width: 600px) {
.header {
  margin-left: 10px;
  &__nav {
      img {
          margin-top: 15px;
          margin-left: 0px;
      }
    // position: relative;
  }
  &__navbar {
    display: flex;
    // align-items: center;
    // justify-content: flex-end;
  }
  &__item {
    padding: 1rem;
  }

  &--button {
    bottom: 10px;
    right: 5px;
    position: absolute;
    color: gray;
    cursor: pointer;
    border: 1px solid transparent;
    background-color: transparent;
    &:focus {
      outline: 0;
    }
  }
}
}


// Dropdown Menu

.dropdown__menu {
  transition: transform 300ms linear;
  top: 80%;
  right: 0;
  position: absolute;
  z-index: 10;
  height: 15rem;
  min-width: 200px;
  margin-top: 1rem;
  overflow-y: auto;
  padding: 5px 5px;
  background-color: #ffffff7c;
  border: 1px solid var(--color-gray);
  background-clip: padding-box;
  
//   li {
//     list-style-type: none;
//     font-size: 20px;
//     font-weight: bold;
//     padding-bottom: 25px;
//     padding: 0px 0px 8px 0px;
//   }
  a {
    text-decoration: none;
    color: rgb(94, 88, 88);
  }
  div {
      color: rgb(94, 88, 88);
     font-size: 20px;
    font-weight: 500;
   
    padding: 0px 0px 4px 0px;
  }
}
</style>>