<template>
<div>
<div class="contain" id="services">
    <div class="contain-head">
        <h3>Services</h3>
    </div>
    <div class="flex">
        <div class="card"  v-for="(image,) in images" :key="image.id" data-aos="fade-up" data-aos-duration="1000">
            <div class="card-img">
                <img :src="image.img1" />
            </div>
            <div class="card-content">
                <h3>{{image.hearder}}</h3>
                <p>{{image.text}}</p>
            </div>  
        </div>
    </div>
    <div class="flex2"  data-aos="fade-up" data-aos-duration="1000">
        <div class="flex2-card2">
            <div class="flex2-card2--header">
                <h2>Normal Service</h2>
            </div>
            <div class="flex2-card2--text">
                <p>Pickup or delivery in 7 working days after payment</p>
            </div>
        </div>
        <div class="flex2-card2">
            <div class="flex2-card2--header">
                <h2>Express Services + 3000</h2>
            </div>
            <div class="flex2-card2--text">
                <p>Pickup or delivery in 3days after payment</p>
            </div>
        </div>
        <div class="flex2-card2">
            <div class="flex2-card2--header">
                <h2>Super Express+ ₦5000</h2>
            </div>
            <div class="flex2-card2--text">
                <p>Pickup or delivery in 7 working days after payment</p>
            </div>
        </div>
    </div>
</div>
</div>
</template>

<script>
export default {
    component: {},
    data() {
        return {
            images: [
                {
                    id: 1,
                    img1: require("../assets/img/istockphoto-1225622316-612x612.jpg"),
                    hearder: "Custom Tailoring",
                    text: "We provide custom tailoring service so that you can choose all details you want, from buttons to pockets and lapels, we can do everything."
                },
                {
                    id: 2,
                    img1: require("../assets/img/360_F_263716591_zTcUirQIQdfWmcgSuCbkG643MefuVGHL.jpg"),
                    hearder: "Alteration",
                    text: "The perfect cut for your outfit is something we believe in. We are engaged in offering best altering options helping you look more classy."
                    
                },
                {
                    id: 3,
                    img1: require("../assets/img/portrait-african-american-female-fashion-260nw-568325581.jpg"),
                    hearder: "Wedding Outfit Tailoring",
                    text: "We help you make your big day very special by providing unique and creative designs of stitching making you look as beautiful as you can."
                },
                {
                    id: 4,
                    img1: require("../assets/img/693-06379235en_Masterfile.jpg"),
                    hearder: "Home Visit Tailor Services",
                    text: "We truly understand your busy schedule. Our master experts are available to visit at your place for taking the necessary measurements."
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
.contain {
    background: #f3e8eb75;
    height: 100%;
    width: 100%;
    margin: 10% 0% 30px 0%;
    @media(max-width: 600px) {
        width: 102%;
        // margin: 10% 0% 30px 0%;
    }

    &-head {
        text-align: center;
        font-size: 25px;
        padding: 60px 0px 0px 0px;
        color: #4C4556;
    }
}
.flex {
    width:100%;
    display: flex;
    justify-content: space-around;
    margin: 50px 0px 0px 0px;
    @media (max-width:600px) {  
      display: block  
    }


    .card {
        height: 26rem;
        width: 20rem;
        @media (max-width:600px) {  
            margin-bottom: 20px;
            margin-left: 5px;
            width: 23.7rem; 
            height: 27rem; 
        }

        &:hover{
            box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
        }
        
        &-img {
            img {
                width: 20rem;
                @media (max-width:600px) {  
            
            width: 23.5rem;  
        }
            }
        }
        &-content {
            text-align: center;
            padding: 20px;
            color: rgb(63, 60, 60);;

            h3 {
                color: black;
                margin-bottom: 20px;
                font-weight: 750;
                font-size: 18px;
            }
            p {
                font-size: 18px;
            }
        }  
    }
}
.flex2 {
    margin-top: 80px;
    display: flex;
    justify-content: space-around;
    margin-bottom : 50px;
    @media (max-width:600px) {  
      display: block  
    }
    &-card2 {
        height: 400px;
        width: 400px;
        box-shadow: 0 0 50px rgba(0, 0, 0, 0.315);
        // background-image: url("../assets/img/Polygon Luminary.svg");
        position: relative;
        background: #433E49;
        @media (max-width:600px) {  
            margin-bottom: 10px;
            margin-left: 5px;
            width: 23.7rem; 
            height: 16rem; 
        }

        &--header {
            height: 180px;
            width: 200px;
            font-size: 30px;
            text-align: center;
            box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
            position: absolute;
            top: 60px;
            left: 20px;
            background: #433E49;
            @media (max-width: 600px){
                position: absolute;
                padding: 10px;
                top: 30px;
                left: 20px;
                height: 70px;
                font-size: 50px;

            }
            h2 {
                padding: 5px;
                color: #ffff;
                @media(max-width:600px){
                    font-size: 18px;
                }
            }

        }
        &--text {
            height: 150px;
            width: 300px;
            font-size: 30px;
            text-align: center;
            box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
            position: absolute;
            top: 220px;
            left: 80px;
            background: #9284904f;
            @media (max-width: 600px){
                position: absolute;
                top: 85px;
                left: 65px;
                width: 250px;
                color: #ffff;
                padding: 0px;
                font-size: 20px;
                height: 130px;

            }

            p {
                color: #ffff;
                padding: 20px;
            }

        }
    }
}
</style>