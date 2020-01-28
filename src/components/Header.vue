<template>
  <div>
    <header>
      <h1 @click="changeTitle">{{ title }}</h1>
    </header>
  </div>
</template>

<script>
export default {
  props: ["title"],
  data() {
    return {};
  },

  methods: {
    changeTitle() {
      this.$emit("changeTitle", "Vue Wizards");
    }
  }
};
</script>

<style lang="css" scoped>
header {
  background: lightgreen;
  padding: 10px;
}
h1 {
  color: #222;
  text-align: center;
}
</style>
