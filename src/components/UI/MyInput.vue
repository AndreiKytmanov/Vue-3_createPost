<template>
  <input :value="modelValue" @input="updateInput" type="text" class="post_description" />
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
    }
  }
};
</script>

<style scoped>
.post_description {
  width: 100%;
  border: 2px solid teal;
  padding: 15px;
  margin-top: 10px;
}
</style>
