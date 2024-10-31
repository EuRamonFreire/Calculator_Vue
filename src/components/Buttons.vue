<script setup>
const props = defineProps(['updateDisplay','clearDisplay'])
</script>


<template>
    <div class="buttons">
        <div class="row">
            <div class="col-auto">
                <button @click="() => props.updateDisplay('+')" class="btn btn-info">+</button>
                <button @click="() => props.updateDisplay('-')" class="btn btn-info">-</button>
                <button @click="() => props.updateDisplay('*')" class="btn btn-info">*</button>
                <button @click="() => props.updateDisplay('/')" class="btn btn-info">÷</button>
            </div>
        </div>
        <div class="row">
            <div class="col-auto">
                <button @click="() => props.updateDisplay('1')" class="btn btn-warning">1</button>
                <button @click="() => props.updateDisplay('2')" class="btn btn-warning">2</button>
                <button @click="() => props.updateDisplay('3')" class="btn btn-warning">3</button>
                <button class="btn btn-danger" @click="props.clearDisplay">C</button>
            </div>
        </div>
        <div class="row">
            <div class="col-auto">
                <button @click="() => props.updateDisplay('4')" class="btn btn-warning">4</button>
                <button @click="() => props.updateDisplay('5')" class="btn btn-warning">5</button>
                <button @click="() => props.updateDisplay('6')" class="btn btn-warning">6</button>
                <button @click="() => props.updateDisplay('0')" class="btn btn-warning">0</button>

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
</template>