<template>
  <div class="container p-5 calculator">
    <Display :value="inputStr" />
    <Buttons @button-click="updateDisplay" @clear-click="clearDisplay" />
  </div>
</template>

<script>
import Display from './components/Display.vue';
import Buttons from './components/Buttons.vue';
import { ref } from 'vue';

export default {
  components: {
    Display,
    Buttons
  },

  setup() {
    const inputStr = ref('');
    const result = ref(null);

    const updateDisplay = (val) => {
      if (val === '=') {
        calculate();
      } else {
        inputStr.value += val;
      }
    };

    const calculate = () => {
      try {
        result.value = eval(inputStr.value);
        inputStr.value = result.value.toString();
      } catch (e) {
        inputStr.value = 'Error';
      }
    };

    const clearDisplay = () => {
      inputStr.value = '';
    };

    return {
      inputStr,
      updateDisplay,
      calculate,
      clearDisplay
    };
  }
};
</script>

<style scoped>
.calculator {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 2px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 0 20px #0000001a;
  background: #fefefe;
}
</style>
