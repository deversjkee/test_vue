<template>
  <div class="input_flex">
    <input
        type="text"
        class="input"
        :value="modelValue"
        @input="$emit('update:modelValue', $event.target.value)"
    >
    <button
      @click="$emit('update:modelValue', '')"
    >remove</button>
  </div>
</template>

<script setup>
import {defineEmits, defineProps} from 'vue'
  defineProps(['modelValue'])
  defineEmits(['update:modelValue'])
</script>

<style scoped>
.input_flex{
  display: flex;
  justify-content: space-between;
}
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 10px;
}
</style>