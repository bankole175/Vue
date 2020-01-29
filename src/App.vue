<template>
  <div>
    <form-helper>
      <div slot="form-header">
        <h3>Form Title</h3>
        <p>Information Field</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" required />
        <input type="password" placeholder="password" required />
      </div>
      <div slot="form-controls">
        <button @click="handleSubmit">Submit</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import FormHelper from "./components/FormHelper";
export default {
  components: {
    FormHelper
  },
  data() {
    return {};
  }
};
</script>

<style lang="css" scoped></style>
