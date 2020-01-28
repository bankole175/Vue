<template>
  <div>
    <app-header :title="title" @changeTitle="updateTitle($event)" />

    <app-ninjas :ninjas="ninjas" />
    <hr />
    <app-ninjas :ninjas="ninjas" />

    <app-footer :title="title" />
  </div>
</template>

<script>
import Header from "./components/Header";
import Footer from "./components/Footer";
import Ninjas from "./components/Ninjas";
export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    "app-ninjas": Ninjas
  },
  data() {
    return {
      ninjas: [
        { id: 1, name: "Ryan", specialty: "Vue Component", show: false },
        { id: 2, name: "Cras", specialty: "HTML Wizard", show: false },
        { id: 3, name: "Ryan", specialty: "Click Event", show: false },
        { id: 4, name: "Ryan", specialty: "Conditiional", show: false },
        { id: 5, name: "Ryan", specialty: "Webpack Component", show: false },
        { id: 6, name: "Ryan", specialty: "Data Digging", show: false }
      ],

      title: "Vue Ninja Banky"
    };
  },

  methods: {
    updateTitle(updatedTitle) {
      this.title = updatedTitle;
    }
  }
};
</script>

<style lang="css" scoped></style>
