<template>
  <div>
      <div class="header">
          <div class="header-text">
            <h2>We Stitch Designs<br> <span>That Fits You Perfectly...</span></h2>
          </div>
          <div class="header-btn">
              <button>Catalogue</button>
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.header {
    min-height: 700px;
    background: linear-gradient(to right bottom, rgba(68, 66, 66, 0.26), rgba(102, 91, 91, 0.342)), url("../assets/img/pexels-michael-burrows-7147649.jpg");
    background-size: cover;
    background-position: top;
    margin-top: 6%;
    position: relative;
    &-btn {
        text-align: center;
        button {
            margin-top: 28%;
            font-size: 18px;
            padding: 10px 30px;
            border-radius: 50px;
            border: none;
            background: #928490;
            color: #ffff;

            &:hover {
                transform: translateY(-3px)
            }
        }
    }
    &-text {
        position: absolute;
        top: 250px;
        left: 200px;
        color:#ffff;
        font-size: 40px;
        width: 30em;
        white-space: nowrap;/*Evitar saltos de línea*/
        overflow: hidden;
        animation: keyframes 10s steps(500) infinite; 
        @keyframes keyframes{ 
            from{ width: 0px;} 
        } 

        span {
            color: #F3E8EB;
            font-weight: 50;
        }
    }
}
</style>