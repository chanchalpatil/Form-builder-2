<template>
  <div class="container mt-5 mb-5">
    <div class="row">
      <FormAttributes>
      </FormAttributes>
      <Form></Form>
    </div>
  </div>
</template>

<script>
import FormAttributes from "./components/FormAttributes.vue"
import Form from "./components/Form.vue"
export default {
  components: {
    FormAttributes,
    Form
  },
};
</script>

<style scoped>
h6 {
  font-weight: 700;
}
.col {
  height: 90vh;
  overflow: auto;
}
.draggable-list {
  min-height: 10vh;
}
.draggable-list > div {
  cursor: pointer;
}
</style>