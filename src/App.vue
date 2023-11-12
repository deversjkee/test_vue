<template>
  <MyInput
      v-model="text"
  />
  <MyInput
      v-model="text"
  />

  <br>
  <br>

  <div class="result">
    <span>{{text}}</span>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import MyInput from "@/components/MyInput.vue";

const text = ref('')
</script>

<style>
  *{
    margin: 0 auto;
    padding: 0;
    box-sizing: border-box;
    max-width: 680px;
  }
  .app {
    display: flex;
    flex-direction: column;
    margin: 15px;
  }
</style>
