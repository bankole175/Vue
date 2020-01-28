<template>
  <div id="ninjas">
    <ul>
      <li
        v-for="ninja in ninjas"
        :key="ninja.id"
        @click="ninja.show = !ninja.show"
      >
        <h2>{{ ninja.name }}</h2>
        <h3 v-show="ninja.show">{{ ninja.specialty }}</h3>
      </li>
    </ul>
    <button @click="deleteNinja">Delete Ninja</button>
  </div>
</template>

<script>
export default {
  props: {
    ninjas: {
      type: Array,
      required: true
    }
  },
  data() {
    return {};
  },

  methods: {
    deleteNinja() {
      this.ninjas.pop();
    }
  },

  beforeCreated() {
    alert("beforeCreated");
  },

  created() {
    alert("created");
  },

  beforeMount() {
    alert("beforeMount");
  },

  mounted() {
    alert("Mounted");
  },

  beforeUpdate() {
    alert("beforeUpdate");
  },

  update() {
    alert("updated");
  }
};
</script>

<style lang="css" scoped>
#ninjas {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0px 20px;
  box-sizing: border-box;
}

ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
  cursor: pointer;
}
</style>
