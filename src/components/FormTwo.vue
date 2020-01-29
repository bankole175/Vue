<template>
  <div>
    <form>
      <div class="form-fields">
        <input type="text" placeholder="name" required />
        <input type="password" placeholder="password" required />
      </div>
      <div class="form-controls">
        <button @click="handleSubmit">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
form {
  width: 100%;
  max-width: 960px;
  margin: 0 auto;
}
#useful-links ul {
  padding: 0;
}
#useful-links li {
  display: inline-block;
  margin-right: 10px;
}
form > div {
  padding: 20px;
  background: #eee;
  margin: 20px 0;
}
</style>
