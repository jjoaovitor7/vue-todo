<template>
  <div>
    <ToDo />
  </div>
</template>

<script>
import ToDo from "./pages/ToDo";

export default {
  name: "App",
  components: {
    ToDo,
  },
};
</script>

<style scoped>
div {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
