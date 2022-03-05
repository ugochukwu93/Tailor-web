<template>
  <div>
      <div class="book-modal">
        <div class="book-modal--button">
            <button @click="close">Close</button>
        </div>
        <form @submit="submitForm" class="book-modal--form">
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">Full name</label>
                <input type="text" v-model="name" class="form-control  form-control w-75" required/>
                <!-- <div class="invalid-feedback">text required</div> -->
            </div>
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">Phone number</label>
                <input type="number" v-model="number" class="form-control  form-control w-75" required/>
                <div class="invalid-feedback">text required</div>
            </div>
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">Tell us about the style you want</label>
                <input type="text" v-model="styleType" class="form-control  form-control w-75" required/>
                <div class="invalid-feedback">text required</div>
            </div>
            
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">Type of service</label>
                <select v-model="selected" class="form-select  form-select w-75" aria-label="Default select example" required>
                    <!-- <option value="" disabled selected hidden>select type of service</option> -->
                    <option  v-for="service in services">{{service.title}}</option>
                </select>
            </div>
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">How do we get your measurement (required)</label>
                <select v-model="selected2" class="form-select  form-select w-75" aria-label="Default select example" required>
                    <!-- <option value="" disabled selected hidden>select how we get your measurement</option> -->
                    <option selected v-for="service2 in services2">{{service2.title}}</option>
                </select>
            </div>
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">How do we get your fabric (required)</label>
                <select v-model="selected3" class="form-select  form-select w-75" aria-label="Default select example" required>
                    <option selected v-for="service3 in services3">{{service3.title}}</option>
                </select>
            </div>
            <div class="col-12 form-group input">
                <label class="col-form-label col-form-label">How do you want to get your stuff when we finish (required)</label>
                <select v-model="selected4" class="form-select  form-select w-75" aria-label="Default select example" required>
                    <option selected v-for="service4 in services4">{{service4.title}}</option>
                </select>
            </div>
            <div class="input">
                <button>Submit</button>
            </div>
        </form>   
      </div>
  </div>
</template>


<script>


export default {
    components: {
       
    },
    props: {
        modal: Boolean
    },
    data() {
        return{
            name: "",
            number: "",
            styleType: "",
            typeOfService: "",
            getMeasurement: "",
            getFabric: "",
            deliveryMethod: "",
            selected: "",
            selected2: "",
            selected3: "",
            selected4: "",
            services:[
                {
                id:1,
                title: 'Normal -7 working days', 
                },
                {
                id: 2,
                title: 'Express -3 days (+N3000)',
                },
                {
                id: 3,
                title: 'Magic -24 hours (+N5000)',
                },    
                    
            ],  
            services2: [               
                {
                id:1,
                title: 'We should come over (free)', 
                },
                {
                id: 2,
                title: 'You will send it',
                },
                {
                id: 3,
                title: 'I trust US/UK sizes',
                },    
                    
            ],  
            services3:[
                {
                id:1,
                title: 'We should come get it (free)', 
                },
                {
                id: 2,
                title: 'You will send it',
                },
                {
                id: 3,
                title: 'We should buy for you',
                },     
            ],  
            services4:[
                {
                id:1,
                title: 'We should deliver (+N1000)', 
                },
                {
                id: 2,
                title: 'You will come and get it (free)',
                },
            ],  
        }
    },
    
    
    methods: {
        submitForm(){
            let url = `${"https://wa.me/+23407062479020?text="}NAME : 
            ${this.name},PHONE NUMBER :
            ${this.number},STYLE TYPE : 
            ${this.styleType}, TYPE OF SERVICE : 
            ${this.selected}, HOW YOU GET MEASUREMENT : 
            ${this.selected2}, HOW YOU GET FABRICS : 
            ${this.selected3},  HOW I GET FABRIC AFTER IS DONE : 
            ${this.selected4}`

            window.open(url, '_blank').focus();
            this.name = "",
            this.number = "",
            this.styleType = "",
            this.selected = ""
            this.selected2 = ""
            this.selected3 = ""
            this.selected4 = ""
        },
        closeModal() {
            this.modal = false
        },
        
        close(event) {
        this.$emit('close');
        },
    }

}
</script>

<style lang="scss" scoped>

.book-modal {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background: linear-gradient(
      90deg,
      rgba(255, 255, 255, 0.541) 0%,
      rgba(255, 255, 255, 1) 70%,
      
    );
    z-index: 10000;
    overflow: auto;
    @media(max-width: 600px) {
        width:100vw
    }
    &--button{
        margin: 2px 0px 0px 1400px;
        @media(max-width: 600px) {
            margin: 2px 0px 10px 140px;
        }
    }

    &--form {
        background-color: #e9b3c175;
        border-radius: 10px;
        margin: 1px 20%;
        padding: 30px;
        @media(max-width: 600px) {
            margin: 10px ;
            padding: 5px;
        }
    }
}
.input {
    margin: 0% 12%;
    
}
button {
    margin-top: 30px;
    padding: 7px 25px;
    border-radius: 3px;
    border: none;
    background: #433E49;
    color: #ffff;
    @media(max-width: 600px) {
         padding: 5px 15px;
         margin-top: 15px;
         margin-bottom: 15px;
    }
}
label {
    @media(max-width: 600px) {
        width: 275px;
    }
}
</style>