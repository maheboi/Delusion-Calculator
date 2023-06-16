<template>
    <div class="blue-box-races">
      <!-- Heading -->
      <h3 class="heading">Race</h3>
      
      <!-- Checkboxes -->
      <div class="box">
        <input type="checkbox" id="checkbox1" v-model="checkboxValues.checkbox1">
        <label for="checkbox1">White</label>
      </div>
      
      <div class="box">
        <input type="checkbox" id="checkbox2" v-model="checkboxValues.checkbox2">
        <label for="checkbox2">Black</label>
      </div>
      
      <div class="box">
        <input type="checkbox" id="checkbox3" v-model="checkboxValues.checkbox3">
        <label for="checkbox3">Hispanic</label>
      </div>
      
      <div class="box">
        <input type="checkbox" id="checkbox4" v-model="checkboxValues.checkbox4">
        <label for="checkbox4">Asian</label>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'BlueBox-Age',
    components: {
    },
    data() {
      return {
        
        // Checkbox values
        checkboxValues: {
          checkbox1: false,
          checkbox2: false,
          checkbox3: false,
          checkbox4: false,
        },
      };
    },
   
  };
  </script>
  
  <style scoped>
  .blue-box-races {
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

.box{
color: white;
transform: translateX(15px);

text-align: left;

}


</style>






