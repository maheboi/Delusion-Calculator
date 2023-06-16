<template>
  <div class="blue-box-age">
    <!-- Heading -->
    <h3 class="heading">Age</h3>
    
    <!-- Slider component -->
    <vue-slider v-model="sliderRange" :min="0" :max="75" :range="true" class="slider-right" :style="{ width: '300px' }"></vue-slider>
    
    <!-- Lower value box -->
    <div class="box box-left">
      Lower Value:
      <input v-model="lowerValue" type="number" @input="updateSliderRange">
    </div>
    
    <!-- Upper value box -->
    <div class="box box-right">
      Upper Value:
      <input v-model="upperValue" type="number" @input="updateSliderRange">
    </div>
  </div>
</template>

<script>
import VueSlider from 'vue-slider-component';
import 'vue-slider-component/theme/default.css';

export default {
  name: 'BlueBox',
  components: {
    VueSlider
  },
  data() {
    return {
      // Initial lower and upper values of the slider
      sliderRange: [0, 75],
      
      // Initial value for the lower box
      lowerInput: 0,
      
      // Initial value for the upper box
      upperInput: 75,
    };
  },
  computed: {
    lowerValue: {
      // Getter function for lowerValue
      get() {
        return this.sliderRange[0];
      },
      
      // Setter function for lowerValue
      set(value) {
        this.lowerInput = value;
      },
    },
    upperValue: {
      // Getter function for upperValue
      get() {
        return this.sliderRange[1];
      },
      
      // Setter function for upperValue
      set(value) {
        this.upperInput = value;
      },
    },
  },
  methods: {
    updateSliderRange() {
      // Parse lower and upper values as integers
      const lower = parseInt(this.lowerInput);
      const upper = parseInt(this.upperInput);

      // Update sliderRange if both values are valid numbers
      if (!isNaN(lower) && !isNaN(upper)) {
        this.sliderRange = [lower, upper];
      }
    },
  },
};
</script>

<style scoped>
.blue-box-age {
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

.slider-right {
  margin-top: 15px;
  transform: translateX(50px);
}

.container {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.box {
  padding: 5px;
  margin-top: 5px;
}

.box-left {
  align-self: flex-start;
  color: white;
}

.box-right {
  align-self: flex-end;
  color: rgb(255, 255, 255);
  
 
 
}

</style>