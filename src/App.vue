<template>
  <div id="app" class="container">
    <ToDoList/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import ToDoList from "./components/ToDoList";

export default {
  name: "App",
  components: {
    HelloWorld, ToDoList
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}
#app {
  font-family: "Montserrat", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
