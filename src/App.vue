<template>
  <div class="App">
    <Header />
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}

header {
  width: 100%;
  height: 200px;
  background-color: rgb(116, 2, 2);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h2 {
  font-size: 50px;
  color: white;
  margin-bottom: 10px;
}

section {
  width: 80%;
  display: flex;
  justify-content: center;
  align-items: center;
}

input {
  width: 80%;
  padding: 15px;
  font-size: 20px;
  border: none;
  outline: none;
  border-radius: 3px;
}

button {
  width: 100px;
  padding: 15px;
  font-size: 20px;
  outline: none;
  border: 1px solid white;
  background-color: transparent;
  color: white;
  border-radius: 3px;
  cursor: pointer;
}

main {
  display: inline-flex;
  flex-wrap: wrap;
  gap: 30px;
}

.card {
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 400px;
  height: 650px;
  border-radius: 3px;
  box-shadow: 1px 3px 3px 1px rgba(0, 0, 0, 0.26);
  margin: 20px;
}

.card img {
  width: 100%;
  height: 200px;
  border-radius: 3px;
  object-position: center;
  object-fit: cover;
}

.card h3 {
  font-size: 18px;
  margin: 0 20px;
}

.card ul {
  list-style: none;
  margin: 0 20px;
}

.card a {
  text-decoration: none;
  color: white;
  background-color: rgb(116, 2, 2);
  border-radius: 3px;
  padding: 10px;
  margin: 0 20px;
  width: 80px;
}
</style>
