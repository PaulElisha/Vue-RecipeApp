<template>
  <header>
    <h2>Vue Recipe App</h2>
    <section>
      <input
        type="text"
        placeholder="search recipe..."
        v-model.trim="searchValue"
      />
      <button @click="getData">Search</button>
    </section>
  </header>
  <Main :data="data" />
</template>

<script>
import Main from "./Main.vue";
import axios from "axios";

export default {
  name: "Header",
  components: {
    Main,
  },
  data() {
    return {
      searchValue: "",
      data: [],
    };
  },
  methods: {
    async getData() {
      try {
        const response = await axios.get(
          `https://api.edamam.com/search?q=${this.searchValue}&app_id=7aa516a5&app_key=dc836a223fb788b11ae390504d9e97ce&from=0&to=10`
        );
        const data = await response.data;
        console.log(data.hits);
        this.data = data.hits;
        this.searchValue = "";
      } catch (err) {
        console.log(err);
      }
    },
  },
};
</script>

<style></style>
