<template>
    <div class="blue-box-married">
      <!-- Heading -->
      <h3 class="heading">Include Married Men?</h3>
      
      <!-- Checkboxes -->
      <div class="box">
        <input type="checkbox" id="checkbox1" v-model="checkboxValues.checkbox1" @change="handleCheckboxChange('checkbox1')">
        <label for="checkbox1">Yes</label>
      </div>
      
      <div class="box">
        <input type="checkbox" id="checkbox2" v-model="checkboxValues.checkbox2" @change="handleCheckboxChange('checkbox2')">
        <label for="checkbox2">No</label>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'BlueBox-Married',
    data() {
      return {
        // Checkbox values
        checkboxValues: {
          checkbox1: false,
          checkbox2: false
        },
      };
    },
    methods: {
      handleCheckboxChange(checkboxId) {
        if (this.checkboxValues.checkbox1 && this.checkboxValues.checkbox2) {
          // If both checkboxes are selected, uncheck the one that was clicked last
          if (checkboxId === 'checkbox1') {
            this.checkboxValues.checkbox2 = false;
          } else if (checkboxId === 'checkbox2') {
            this.checkboxValues.checkbox1 = false;
          }
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .blue-box-married {
    width: 400px;
    height: 150px;
    background-color: #354759;
    border-radius: 50px;
  }
  
  .heading {
    margin: -10px 0 0;
    color: white;
    text-align: left; /* Align the heading to the left */
    padding-left: 40px; /* Add some left padding to move it to the right */
    padding-top: 10px;
  }
  
  .container {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
  }
  
  .box {
    color: white;
    transform: translateX(15px);
    text-align: left;
  }
  </style>