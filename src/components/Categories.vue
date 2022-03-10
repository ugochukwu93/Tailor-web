<template>
  <div id="categories">
      <div class="categories" >
        <h2>Categories</h2>
      </div>
    <div class="container">
        <div class="item item--1"  data-aos="fade-up" data-aos-duration="1000"><img src="../assets/img/unnamed-removebg-preview.png"/><div><h3>Ankara Gown With Styles</h3></div></div>
        <div class="item item--2"  data-aos="fade-up" data-aos-duration="1000"><img src="../assets/img/ankara-styles-2-removebg-preview.png"/><div><h3>Ankara Mini Gown</h3></div></div>
        <div class="item item--3"  data-aos="fade-up" data-aos-duration="1000"><img src="../assets/img/yellow-skirt.png"/><div><h3>Office Top And Skirt</h3></div></div>
        <div class="item item--4"  data-aos="fade-up" data-aos-duration="1000"><img src="../assets/img/9e99sj3w-removebg-preview.png"/><div><h3>Office Top And Skirt</h3></div></div>
        <div class="item item--5"  data-aos="fade-up" data-aos-duration="1000"><img src="../assets/img/african-print-office-10-removebg-preview.png"/><div><h3>Skirt And Top</h3></div></div>
        <div class="item item--6"  data-aos="fade-up" data-aos-duration="1000"><img src="../assets/img/618253-removebg-preview.png"/><div><h3>Office Gown</h3></div></div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.categories {
    text-align: center;
    font-size: 25px;
    margin: 60px 0px 60px 0px;
    color: #4C4556;
}
.container {
//   background-color:#eee;
  width: 1100px;
  margin: 20px auto;
  
  display: grid;
  //grid-template-rows: repeat(2, 1fr);
  grid-template-rows: repeat(2, 500px);
  //grid-template-columns: repeat(2, 150px) 1fr;
  //grid-template-columns: 50% 1fr 1fr;
  grid-template-columns: repeat(3, 1fr);
  //grid-row-gap: 30px;
  //grid-column-gap: 30px; 
  grid-gap: 100px; //combines previous two lines if same

   @media (max-width:600px) {  
      width: 348px; 
      margin-bottom:20px ; 
      display: block;
      padding-right: 0px;
      padding-left: 0px;
      //  margin: 10px 0px 10px 10px;
         
  }
}

.item {
  padding: 20px;
  height: 500px;
  font-size: 20px;
  font-family: sans-serif;
  color: #fff;
  position: relative;
  
  @media(max-width: 600px) {
    width: 100%;
  }

  div {
    transform: rotate(270deg);
      height: 70px;
      width: 500px;
      position: absolute;
      background: #4C4556;
      left: 50px;
      top: 230px;
      h3 {
        text-align: center;
        margin-top: 20px;
        font-family: "Lucida Console", "Courier New", monospace;
         

      }
  }
  
  &--1 {
    background-color: #F3E8EB;
    /*grid-row-start: 2;
    grid-row-end: 3;
    grid-column-start: 2;
    grid-column-end: 3;*/
    grid-row: 2 / 3;
    grid-column: 2 / 3;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    @media (max-width:600px) {  
      margin-bottom: 20px;   
    }

    img {
        position: absolute;
        right: 0px;
        top: 0px;
        height: 500px
    }

    &:hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }

  }
  
  &--2 {
     background-color: #F3E8EB;
     //grid-column: 2 / span 2;
    grid-column: 1 / 2; //spans from 2 to end
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    @media (max-width:600px) {  
      margin-bottom: 20px;   
    }
    
    img {
        position: absolute;
        right: 0px;
        top: 0px;
        height: 500px
    }

    &:hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    } 
  }
  
  &--3 {
    background-color: #F3E8EB;
    grid-row: 2 / 3;
    grid-column: 1 / 2;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    @media (max-width:600px) {  
      margin-bottom: 20px;   
    }

    img {
        position: absolute;
        right: 0px;
        top: 0px;
        height: 500px
    }


    &:hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }
   
  }
  
  &--4 {
    background-color: #F3E8EB;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    @media (max-width:600px) {  
      margin-bottom: 20px;   
    }

    img {
        position: absolute;
        right: 0px;
        top: 0px;
        height: 500px
    }

    &:hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }
    
  }
  
  &--5 {
    background-color: #F3E8EB;
    /*grid-row: 1 / 2;
    grid-column: 3 / 4;*/
    grid-area: 1 / 3 / 2 / 4; // r-start c-s r-end c-e
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    @media (max-width:600px) {  
      margin-bottom: 20px;   
    }

    img {
        position: absolute;
        right: 0px;
        top: 0px;
        height: 500px
    }

    &:hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }
    
  }
  
  &--6 {
    background-color: #F3E8EB;
    //grid-area: 1 / 2 / 2 / 3;
    grid-row: 1 / 2;
    grid-column: 2 / 3;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    @media (max-width:600px) {  
      margin-bottom: 20px;  
    }

    img {
        position: absolute;
        right: 0px;
        top: 0px;
        height: 500px
    }

    &:hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }
    
  }
}

</style>