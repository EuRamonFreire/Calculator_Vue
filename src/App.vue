<template>

<body>
  <div class="container p-5">
    <div class="display">
      <form class="form-group" action="" @submit.prevent="calculate">
        <input class="screen" type="text" v-model="inputStr">
        <input class="equali" type="submit" value="=">
      </form>
    </div>
    <div class="buttons">
      <div class="row">
        <div class="col-auto">
          <button @click="() => updateDisplay('+')" class="btn btn-info">+</button>
          <button @click="() => updateDisplay( '-')" class="btn btn-info">-</button>
          <button @click="() => updateDisplay('*')" class="btn btn-info">*</button>
          <button @click="() => updateDisplay('/')" class="btn btn-info">÷</button>
        </div>
      </div>
      <div class="row">
        <div class="col-auto">
          <button @click="() => updateDisplay('1')"  class="btn btn-warning">1</button>
          <button @click="() => updateDisplay('2')" class="btn btn-warning">2</button>
          <button @click="() => updateDisplay('3')" class="btn btn-warning">3</button>
          <button class="btn btn-danger" @click="clearDisplay">C</button>
        </div> 
      </div>
      <div class="row">
        <div class="col-auto">
          <button @click="() => updateDisplay('4')" class="btn btn-warning">4</button>
          <button @click="() => updateDisplay('5')" class="btn btn-warning">5</button>
          <button @click="() => updateDisplay('6')" class="btn btn-warning">6</button>
          <button @click="() => updateDisplay('0')" class="btn btn-warning">0</button>

        </div> 
      </div>
      <div class="row">
        <div class="col-auto">
          <button @click="() => updateDisplay('7')" class="btn btn-warning">7</button>
          <button @click="() => updateDisplay('8')" class="btn btn-warning">8</button>
          <button @click="() => updateDisplay('9')" class="btn btn-warning">9</button>
          <button @click="() => updateDisplay('.')" class="btn btn-warning">.</button>
          
        </div> 
      </div>
    </div>
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

  .screen{
    height: 50px;
    width: 160px;
    margin-bottom: 2px;
    margin-right: 4px;
    border-radius: 8px;
  }
  /* .display{
    height: 45px;
    width: 165px;
    border-radius: 8px;
    margin-bottom: 10px;
    
  } */


</style>

<script >

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

    calculate () {
      this.result = eval(this.inputStr)
      this.inputStr = this.result
    },

    clearDisplay() {
      this.inputStr = ''
    }
  },
}

</script>