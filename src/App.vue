<template>
  <my-input
      v-model="text"
  />
  <my-input
      v-model="text"
  />

  <br>
  <br>

  <div class="result">
    <span>{{text}}</span>
  </div>
</template>

<script>
import MyInput from './components/MyInput.vue'
import {ref} from "vue";

export default {
  name: 'App',
  components: {
    MyInput
  },
  setup(){
    const text = ref();

    return {
      text
    }
  }
}
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
