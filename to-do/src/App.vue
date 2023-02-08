<template>
  <Board />
</template>

<script>
import Board from "./components/Board.vue";

export default {
  name: "App",
  components: { Board },
};
</script>

<style>
body {
  background: linear-gradient(to right, pink, purple);
}
#app {
  color:white;
  display: flex;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}
</style>
