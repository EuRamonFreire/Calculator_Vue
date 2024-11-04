<template>
  <div class="buttons">
    <button @click="clearClick" class="btn-clear">C</button>
    <button @click="buttonClick('/')">/</button>
    <button @click="buttonClick('*')">*</button>
    <button @click="buttonClick('-')">-</button>
    <button @click="buttonClick('7')">7</button>
    <button @click="buttonClick('8')">8</button>
    <button @click="buttonClick('9')">9</button>
    <button @click="buttonClick('+')">+</button>
    <button @click="buttonClick('4')">4</button>
    <button @click="buttonClick('5')">5</button>
    <button @click="buttonClick('6')">6</button>
    <button @click="buttonClick('0')">0</button>
    <button @click="buttonClick('1')">1</button>
    <button @click="buttonClick('2')">2</button>
    <button @click="buttonClick('3')">3</button>
    <button @click="buttonClick('.')">.</button>
    <button @click="buttonClick('=')" class="btn-equal">=</button>
  </div>
</template>

<script>
export default {
  name: 'Buttons',
  methods: {
    buttonClick(val) {
      this.$emit('button-click', val);
    },
    clearClick() {
      this.$emit('clear-click');
    }
  }
}
</script>

<style scoped>
.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 20px;
  font-size: 1.5em;
  background: #fff;
  border: 2px solid #ccc;
  border-radius: 5px;
  box-shadow: 2px 2px 5px #aaa;
  transition: background 0.3s;
}

button:hover {
  background: #e0e0e0;
}

button:active {
  background: #d0d0d0;
}

.btn-clear {
  background: #f44336;
  color: #fff;
}

.btn-equal {
  grid-column: span 2;
  background: #4caf50;
  color: #fff;
}
</style>
