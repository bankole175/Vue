<template>
  <div>
    <footer>
      <p>{{ copyright }} {{ title }}</p>
    </footer>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    }
  },
  data() {
    return {
      copyright: "Copyright 2020"
    };
  }
};
</script>

<style lang="css" scoped>
footer {
  background: #222;
  padding: 6px;
}
p {
  color: lightgreen;
  text-align: center;
}
</style>
