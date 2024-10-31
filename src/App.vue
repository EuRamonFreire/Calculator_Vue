<template>

  <body>
    <div class="container p-5">

      <Buttons />
      <Display />

    </div>
  </body>

</template>

<style>
.container {
  width: 100%;
  margin-top: auto;
  /* position: relative; */
  left: 25%;
}

.btn {
  margin: 2px;
  width: 50px;
  height: 50px;
}

.equali {
  width: 50px;
  height: 50px;
  color: #fff;
  background-color: green;
  border-style: none;
  border-radius: 8px;
}

.display {
  display: inline-flex;
}

.screen {
  height: 50px;
  width: 160px;
  margin-bottom: 2px;
  margin-right: 4px;
  border-radius: 8px;
}
</style>

<script>
import Display from './components/Display.vue';
import Buttons from './components/Buttons.vue';

export default {
  data() {
    return {
      inputStr: '',
      result: ''
    }
  },

  methods: {
    updateDisplay(val) {
      this.inputStr = this.inputStr + val
    },

    calculate() {
      this.result = eval(this.inputStr)
      this.inputStr = this.result
    },

    clearDisplay() {
      this.inputStr = ''
    }
  },
}

</script>