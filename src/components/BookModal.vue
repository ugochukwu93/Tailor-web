<template>
  <div>
      <div class="book-modal">
          <div class="book-modal--button">
              <button>Close</button>
          </div>
          <div class="book-modal--inputbox">
            <FormData
        v-bind="{
            aboutStyle: about.aboutStyle,
            label: about.label,
            placeholder: about.placeholder,  
        }"
        />
        <select-form
        v-bind="{
            services: services.options,
            label: services.label,
            placeholder: services.placeholder, 
             
        }"
        />
        <select-form
        v-bind="{
            services: services2.options,
            label: services2.label,
            placeholder: services2.placeholder, 
             
        }"
        />
        <select-form
        v-bind="{
            services: services3.options,
            label: services3.label,
            placeholder: services3.placeholder, 
             
        }"
        />
        <select-form
        v-bind="{
            services: services4.options,
            label: services4.label,
            placeholder: services4.placeholder, 
             
        }"
        />
        <FormData
        v-bind="{
            label: service.label,
            placeholder: service.placeholder,   
        }"
        />
        <input type="submit" @click="submitForm()"/>
        <!-- <label for="country">Type of service you want (required)</label>
        <select id="country" name="country">
            <option value="australia">Normal- 7 working days</option>
            <option value="canada">Express - 3 days(+N3000</option>
            <option value="usa">Magic - 24 hours (+N5000</option>
        </select> -->
        <!-- <FormData/>
        <FormData/>
        <FormData/> -->
          </div>
      </div>
  </div>
</template>

<script>
import FormData from './FormData.vue'
import SelectForm from './SelectForm.vue'
export default {
    components: {
        FormData,
        SelectForm,
    },
    data() {
        return {
            about: {
                aboutStyle: "",
                label: "Tell us about the style you want",
                placeholder: "About you.."
            },
            service: {
                typeOfService: "",
                label: "Type of service",
                placeholder: "Sevices",
            },
            services: {
                label: 'Type of service',
                placeholder: "Sevices",
                options:[
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
                    title: 'Magic -@$ hours (+N5000)',
                    },    
                    
                ],  
            },
            services2: {
                label: 'How do we get your measurement (required)',
                placeholder: "",
                options:[
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
            },
            
            services3: {
                label: 'How do we get your fabric (required)',
                placeholder: "",
                options:[
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
                    title: 'We should buy for you',
                    },    
                    
                ],  
            },
            services4: {
                label: 'How do you want to get your stuff when we finish (required)',
                placeholder: "",
                options:[
                    {
                    id:1,
                    title: 'We should deliver (+N1000)', 
                    },
                    {
                    id: 2,
                    title: 'You will come and get it',
                    },
                ],  
            },

            submitForm(){
                 let url = `${"https://wa.me/+23407062479020?text="}${this.about.aboutStyle}`
                 window.open(url, '_blank').focus();
            
        }
    
            
            
        }
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
    // display: flex;
    // align-items: center;
    overflow: auto;

    &--inputbox {
        background: white;
        margin: 8% 20% 5% 20%;
        padding: 20px 0px 20px 0px;
        border-radius: 30px;
    }
}
</style>