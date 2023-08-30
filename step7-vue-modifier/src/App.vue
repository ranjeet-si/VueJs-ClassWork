<template>
  <div class="container">
    <input class="range-input" type="range" v-model.number="power">
    <input class="range-input" type="range" v-model.number="booster">
    <button @click.stop="calculateTotal" class="calculate-button">Calculate Total</button>
    <div class="output">
      <div>Power is: {{ power }}</div>
      <div>Booster is: {{ booster }}</div>
      <div>Total Power: {{ totalPower }}</div>
    </div>
    <input class="text-input" v-model.trim.lazy="textInput" placeholder="Type something...">
    <div class="output">
      Trimmed Text: {{ textInput }}
    </div>
  </div>
</template>
 
<script>
export default {
  data() {
    return {
      power: 0,
      booster: 0,
      totalPower: 0,
      textInput: ''
    }
  },
  methods: {
    calculateTotal() {
      this.totalPower = this.power + this.booster;
    }
  }
}
</script>
 
<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.range-input {
  width: 80%;
  margin: 10px;
}

.calculate-button {
  margin: 10px;
}

.text-input {
  width: 80%;
  margin: 10px;
  padding: 5px;
}

.output {
  margin-top: 20px;
  text-align: center;
}
</style>
