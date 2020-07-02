<template>
  <div class="tasklist">
    <span>
      Tarea
      <input placeholder="Ingresar tarea" type="text" v-model="tareas" />
    </span>
    <button @click="add">Crear</button>
    <h2>Lista</h2>
    <ol>
      <li v-for="tareas in array" :key="tareas">{{ tareas }}</li>
    </ol>
  </div>
</template>
<script>
export default {
  name: "tasklist",
  data() {
    return {
      tareas: "",
      array: ["Estudiar"],
    };
  },
  methods: {
    add() {
      if (this.tareas !== "") {
        this.array.push(this.tareas);
        this.tareas = "";
      } else {
        alert("No dejes esto vacío");
      }
    },
  },
};
</script>
<style scoped>
.hellovue {
  padding: 1em;
}
span {
  color: black;
  font-weight: bold;
}
button {
  border: 1px solid black;
  padding: 1px 10px;
  background: white;
  font-weight: bold;
}
h2 {
  color: gray;
  padding: 1em;
}
ol li {
  color: black;
}
</style>
