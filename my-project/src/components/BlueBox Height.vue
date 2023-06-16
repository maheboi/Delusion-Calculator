<template>
    <div class="blue-box-height">
      <!-- Heading -->
      <h3 class="heading">Height</h3>
      
      <!-- Dropdown component -->
      <div class = "dropdown">
        <label for = "dropdown" class = "dropdown-label"> Choose an Option</label>
      <select v-model="selectedValue" class="dropdown-box">
        <option v-for="option in options" :value="option.value" :key="option.value">{{ option.label }} </option>
      </select>
    </div>
    
    </div>
  </template>
  
  <script>
  export default {
    name: 'BlueBox-Height',
    data() {
      return {
        // Initial selected value of the dropdown
        selectedValue: 0,
        
        // Options for the dropdown
        options: [
          { label: 'Option 1', value: 0 },
          { label: 'Option 2', value: 1 },
          { label: 'Option 3', value: 2 },
        ],
      };
    },
    methods: {
      updateSelectedValue() {
        // Parse selected value as an integer
        const value = parseInt(this.selectedValue);
  
        // Update selectedValue if it is a valid number
        if (!isNaN(value)) {
          this.selectedValue = value;
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .blue-box-height {
    width: 400px;
    height: 150px;
    background-color: #354759;
    border-radius: 50px;
  }

  .heading {
    margin: -10px 0 0;
    color: white;
    text-align: left;
    padding-left: 40px;
    padding-top: 10px;
  }
  
  .dropdown-box{
    transform: translateX(10px);
    width: 300px;
    margin: 10px 0 0;
    
    text-align: left;
    padding-left: 40px;
    padding-top: 10px;
  }
  
  .box {
    padding: 5px;
    margin-top: 5px;
  }
  .dropdown-label{
    color: white;
  }
  
 
  </style>