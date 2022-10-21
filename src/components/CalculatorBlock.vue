<template>
  <div>
    <div id="display">
      <input v-model="operand1"/>
      <input v-model="operand2"/>
      = {{result}}
    </div>
    <div class="keyboard">
      <button v-on:click="result = Number(operand1) + Number(operand2)">+</button>
      <button v-on:click="result = operand1 - operand2">-</button>
      <button v-on:click="result = operand1 / operand2">/</button>
      <button v-on:click="result = operand1 * operand2">*</button>
      <button v-on:click="result = Math.pow(operand1, operand2)">x^</button>
      <button v-on:click="result = Math.floor(operand1/operand2)">%</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'CalculatorBlock',
    data(){
      return {
        operand1: 0,
        operand2: 0,
        result: 0
      }
    }
  }
</script>


<style scoped>

</style>
