<script setup>
    const props = defineProps(['inputStr'])
</script>

<template>
    <div class="display">
        <form class="form-group" action="" @submit.prevent="calculate">
            <input class="screen" type="text" v-model="props.inputStr">
            <input class="equali" type="submit" value="=">
        </form>
    </div>
</template>
