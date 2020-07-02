<template>
  <div id="app">
    <h2>
      {{ message }}
    </h2>
    <Tasklist></Tasklist>
  </div>
</template>

<script>
import Tasklist from "./components/TaskList.vue";

export default {
  name: "App",
  components: {
    Tasklist,
  },
  data() {
    return {
      message: "Nueva tarea",
      name: "",
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  scroll-behavior: smooth;
}

body {
  background: rgba(255, 255, 255, 0.87);
}
</style>
