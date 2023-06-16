<template>
  <div id="app">
    <div class="box-row">
      <blue-box-age class="box-margin"></blue-box-age>
      <blue-box-height class="box-margin"></blue-box-height>
      <blue-box-income class="box-margin"></blue-box-income>
    </div>
    <div class="box-row">
      <blue-box-races class="box-margin"></blue-box-races>
      <blue-box-dwelling class="box-margin"></blue-box-dwelling>
      <blue-box-schooling class="box-margin"></blue-box-schooling>
    </div>
    <div class="box-row">
      <blue-box-obese class="box-margin"></blue-box-obese>
      <blue-box-married class = "box-margin"></blue-box-married>
    </div>
  </div>
</template>

<script>
import BlueBoxHeight from './components/BlueBox Height.vue';
import BlueBoxIncome from './components/BlueBox Income.vue';
import BlueBoxAge from './components/BlueBox Age.vue';
import BlueBoxRaces from './components/BlueBox Races.vue';
import BlueBoxDwelling from './components/BlueBox Dwelling.vue';
import BlueBoxSchooling from './components/BlueBox Schooling.vue';
import BlueBoxObese from './components/BlueBox Obese.vue';
import BlueBoxMarried from './components/BlueBox Married.vue';
export default {
  name: 'App',
  components: {
    BlueBoxAge,
    BlueBoxIncome,
    BlueBoxHeight,
    BlueBoxRaces,
    BlueBoxDwelling,
    BlueBoxSchooling,
    BlueBoxObese,
    BlueBoxMarried
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #122f4c;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.box-row {
  /* Add margin to create spacing between rows */
  margin-top: 20px;
  display: flex;
  justify-content: center;
}

.box-margin {
  margin: 20px;
}
</style>