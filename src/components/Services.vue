<template>
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
    <div class="flex2"  data-aos="fade-up" data-aos-duration="1000" v-if="mobileView">
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
    <div class="accordion-menu"  v-if="!mobileView">
        <ul>
            <li>
                <input type="checkbox" checked>
                <i class="arrow"></i>
                <h2><img src="../assets/img/clock1.png" alt="" width="25"/> Normal Service</h2>
                <p>Pickup or delivery in 7 working days after payment
                </p>
            </li>
            <li>
                <input type="checkbox" checked>
                <i class="arrow"></i>
                <h2><img src="../assets/img/fast-time.png" alt="" width="25"/> Express Services + 3000</h2>
                <p>Pickup or delivery in 3days after payment</p>
            </li>
            <li>
                <input type="checkbox" checked>
                <i class="arrow"></i>
                <h2><img src="../assets/img/quick-response.png" alt="" width="25"/> Super Express+ ₦5000</h2>
                <p>Pickup or delivery in 7 working days after payment</p>
            </li>
        </ul>
    </div>
</div>
</template>

<script>
export default {
    component: {},

    data() {
        return {
            mobileView: null,
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
    },
    methods: {
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
.contain {
    background: #f3e8eb75;
    height: 100%;
    width: 100%;
    // margin: 10px 0px 30px 0px;
    padding: 10px 0px 30px 0px;
    @media(max-width: 600px) {
        width: 100%;
        height: 100%;
        margin: 10px 0px 0px 0px;
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
      display: block;
       margin: 50px 0px 0px 0px;
       padding: 20px;
    }


    .card {
        height: 26rem;
        width: 20rem;
        @media (max-width:600px) {  
            margin-bottom: 30px;
            // margin-left: 50px;
            // margin-right: 150px;
            width: 100%; 
            height: 27rem; 
        }

        &:hover{
            box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
        }
        
        &-img {
            img {
                width: 20rem;
                @media (max-width:600px) {  
                    width: 100%;  
                }
            }
            @media (max-width:600px) {  
                width: 100%;  
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
    padding-bottom : 50px;
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
            // margin-left: 5px;
            position: relative;
            width: 335px; 
            height: 240px; 
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
.accordion-menu {
	display: inline-block;
    position: relative;
	left: 50%;
	margin: 0px 0px 60px 0px;
	transform: translate(-50%, 0);
	max-width: 700px;
    padding: 0px 20px 15px;
	// border-radius: 5px;
}
h2 {
	font-size: 18px;
	line-height: 34px;
	font-weight: 500;
	letter-spacing: 1px;
	display: block;
	margin: 0;
    cursor: pointer;
    color: #6c6c6a;
}
p {
	color: rgba(48, 69, 92, 0.8);
	font-size: 15px;
	line-height: 26px;
	letter-spacing: 1px;
	position: relative;
	overflow: hidden;
	max-height: 800px;
	opacity: 1;
	transform: translate(0, 0);
	margin-top: 14px;
	z-index: 2;
}
ul {
	list-style: none;
	perspective: 900;
	padding: 0 20px 10px;
    margin: 0;
    background-color: #fff;
	border-radius: 5px;
	box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.2), 
	0 2px 2px 0 rgba(255, 255, 255, 0.19);
}
ul li {
	position: relative;
	padding: 0;
	margin: 0;
	padding-bottom: 4px;
	padding-top: 18px;
    border-top: 1px dotted #dce7eb;
}

ul li:nth-child(1){ border:none; }
ul li:nth-of-type(1) { animation-delay: 0.5s; }
ul li:nth-of-type(2) { animation-delay: 0.75s; }
ul li:nth-of-type(3) { animation-delay: 1.0s; }
ul li:last-of-type { padding-bottom: 0; }

ul li .arrow {
	position: absolute;
	transform: translate(-6px, 0);
	margin-top: 16px;
	right: 0;
}
ul li .fas{
	// color:#f6483b;
	font-size: 15px;
	margin-right: 10px;
}
ul li .arrow:before, ul li .arrow:after {
	content: "";
	position: absolute;
	background-color: #4C4556;
	width: 3px;
	height: 9px;
}
ul li .arrow:before {
	transform: translate(-2px, 0) rotate(45deg);
}
ul li .arrow:after {
	transform: translate(2px, 0) rotate(-45deg);
}
ul li input[type=checkbox] {
	position: absolute;
	cursor: pointer;
	width: 100%;
	height: 100%;
    z-index: 1;    
    opacity: 0;
}
ul li input[type=checkbox]:checked ~ p {
	margin-top: 0;
	max-height: 0;
	opacity: 0;
	transform: translate(0, 50%);
}
ul li input[type=checkbox]:checked ~ .arrow:before {
	transform: translate(2px, 0) rotate(45deg);
}
ul li input[type=checkbox]:checked ~ .arrow:after {
	transform: translate(-2px, 0) rotate(-45deg);
}
.transition, p, ul li .arrow:before, ul li .arrow:after {
	transition: all 0.25s ease-in-out;
}

.flipIn, h1, ul li {
	animation: flipdown 0.5s ease both;
}
.no-select, h2 {
	-webkit-tap-highlight-color: transparent;
	-webkit-touch-callout: none;
	user-select: none;
}
@keyframes flipdown {
	0% {
		opacity: 0;
		transform-origin: top center;
		transform: rotateX(-90deg);
	}

	5% { opacity: 1; }

	80% { transform: rotateX(8deg); }

	83% { transform: rotateX(6deg); }

	92% { transform: rotateX(-3deg); }

	100% {
		transform-origin: top center;
		transform: rotateX(0deg);
	}
}
</style>