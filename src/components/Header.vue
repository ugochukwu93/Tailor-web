<template>
  <div>
      <div class="header">
          <div class="header-text">
            <h2>We Stitch Designs<br> <span>That Fits You Perfectly...</span></h2>
          </div>
          <div class="header-btn">
              <button @click="openLink('https://www.instagram.com/tailorcatalogue/')">Catalogue</button>
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
.header {
    height: 100vh;
    background: linear-gradient(to right bottom, rgba(68, 66, 66, 0.26), rgba(102, 91, 91, 0.342)), url("../assets/img/pexels-michael-burrows-7147649.jpg");
    background-size: cover;
    background-position: top;
    margin-top: 0%;
    position: relative;
    @media(max-width: 600px) {
        height: 100vh;
    }
    &-btn {
        text-align: center;
        button {
            margin-top: 28%;
            font-size: 18px;
            padding: 10px 30px;
            border-radius: 50px;
            border: none;
            background: #F3E8EB;
            color: #433E49;
            @media(max-width: 600px) {
                margin: 790px 230px 0px 0px;
                border-radius: 5px;
                font-weight: bold;
            }

            &:hover {
                transform: translateY(-3px)
            }
        }
    }
    &-text {
        position: absolute;
        top: 400px;
        left: 200px;
        color:#ffff;
        font-size: 70px;
        width: 7em;
        white-space: nowrap;/*Evitar saltos de línea*/
        overflow: hidden;
        animation: keyframes 10s steps(500) infinite; 
        @keyframes keyframes{ 
            from{ width: 0px;} 
        } 
        @media(max-width: 600px) {
            position: absolute;
            top: 450px;
            left: 50px;
            width: 8em;
            font-size: 40px;
        }

        span {
            color: #F3E8EB;
            font-weight: 50;
        }
    }
    @media only screen and (max-width: 800px) {
        body {
            // background-color: lightblue;
        }
    }
}
</style>