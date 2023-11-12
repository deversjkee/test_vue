<template>
  <my-input
      v-model="inputText"
  />
  <my-input
      v-model="inputText"
  />

  <br>
  <br>

  <div class="result">
    <span>{{inputText}}</span>
  </div>
</template>

<script>
import MyInput from './components/MyInput.vue'

export default {
  name: 'App',
  components: {
    MyInput
  },
  data(){
    return {
      inputText: '',
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
