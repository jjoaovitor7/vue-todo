<template>
  <section id="page-home">
    <Header />
    <TextArea />
    <Tasks />
  </section>
</template>

<script>
import Header from "../components/Header";
import TextArea from "../components/TextArea";
import Tasks from "../components/Tasks";

export default {
  name: "ToDo",
  components: {
    Header,
    TextArea,
    Tasks,
  },
};
</script>

<style scoped src="../styles/ToDo.css"></style>
