<template>
  <div class="board">
    <h3>To Do List</h3>
    <input v-model="name" type="text" />
    <button @click="addTask">Enviar</button>
    <Task :tasks="tasks" />
    {{name}}
  </div>
</template>

<script>
import Task from "./Task.vue";
export default {
  name: "BoardTo",
  components: { Task },
  data() {
    return {
      name:'',
      tasks: [
        {
          name: "Lavar a louça",
          pendente: false,
        },
        {
          name: "Lavar a roupa",
          pendente: true,
        },
      ],
    };
  },
  methods: {
    addTask(task) {
      this.tasks.push({
        name: task.name,
        pendente: task.pendente || true,
      });
    },
  },
};
</script>

<style scopep>
.board {
  background-color: black;
  width: 500px;
  height: 500px;
}

h3 {
  color: white;
  display: flex;
  justify-content: center;
  bottom: 30px;
}

input {
  border: none;
  margin-right: 10px;
  height: 20px;
}

button {
  border: none;
  background-color: pink;
  width: 50px;
  height: 20px;
}

p {
  color: white;
}
</style>