<template>
  <div class="container">
    <div class="input-box">
        <label :for="label">{{label}}</label>
          <input
            @blur="checkForm"
            v-model="aboutStyle"
            :name="label"
            class="input"
            type=""
            :placeholder="placeholder"
          />
          <p class="error">{{errors}}</p>
    </div>
  </div>
</template>

<script>

export default {
  components: { SelectForm },
  data() {
    return {
      text: "",
      errors: "",
    }
  },
  props:{
    label: {
      type: String,
    },
    placeholder: {
      type: String,
    },
    about: {
      type: Object,
    }
  },
  methods:{
    checkForm() {
      if(!this.text){ 
        this.errors="text required."
      } else {
          this.errors = "";
        }
    }
  }
  
}
</script>

<style>

.container {
  align-items: center;
  margin: 0px 30% 0px 30%
}
.input-box {
  width: 100%;
  margin-bottom: 25px;
}
.input-box .input {
  display: block;
  width: 100%;
  padding: 15px;
  color: #313131;
  font-size: 20px;
  appearance: none;
  border: none;
  outline: none;
  background: none;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.15);
  border-radius: 0px 16px 0px 16px;
  transition: 0.4s;
}
.input-box .input:focus {
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.75);
  border-radius: 16px 0px 16px 0px;
}
.error {
  color: red;
  margin-top: 10px;
}
</style>