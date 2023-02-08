<template>
  <div class="tasks">
    <div class="task">
      <div v-for="task in tasks" :key="task.name" >
        <input class="checkbox" type="checkbox" />
        {{ task.name }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Task-Componente",
  props: {
    tasks: { type: Array, required: true },
  },
  computed: {
    styled() {
      return {
        pendente: this.tasks.pendente,
        done: !this.tasks.pendente,
      };
    },
  },

};
</script>

<style scoped>
.tasks {
  padding: 10px;
  cursor: pointer;
  user-select: none;
  padding: 0;
  display: flex;
  justify-content: center;
  align-content: center;
  padding-top: 20px;
  flex-direction: row;
}
.task {
  justify-content: center;
}


</style>