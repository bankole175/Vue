<template>
  <div>
    <keep-alive>
    <component :is="component"></component>
    </keep-alive>
    <button @click="component = 'form-one'">Show Form One</button>
    <button @click="component = 'form-two'">Show Form Two</button>
  </div>
</template>

<script>
import FormOne from "./components/FormOne";
import FormTwo from "./components/FormTwo";
export default {
  components: {
    FormOne,
    FormTwo
  },
  data() {
    return {
      component: "form-one"
    };
  }
};
</script>

<style lang="css" scoped></style>
