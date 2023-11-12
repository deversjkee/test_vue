<template>
  <div class="input_flex">
    <input
        type="text"
        class="input"
        :value="modelValue"
        @input="updateInput"
    >
    <button
      @click="updateInput"
    >remove</button>
  </div>
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event){
      this.$emit('update:modelValue', event.target.value)
    },
  }
}
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