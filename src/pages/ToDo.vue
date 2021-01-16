<template>
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap"
    rel="stylesheet"
  />

  <section id="page-home">
    <Header />
    <TextArea />

    <div id="button-addTask">
      <button @click="addTask" id="btn-ok">Ok</button>
    </div>
    <div class="tasks" v-for="(task, index) in tasks" :key="index">
      {{ task }}
    </div>
  </section>
</template>

<script>
import Header from "../components/Header";
import TextArea from "../components/TextArea";

export default {
  name: "ToDo",
  data() {
    return {
      tasks: [],
    };
  },
  components: {
    Header,
    TextArea,
  },
  methods: {
    addTask() {
      // view model // const vm = this;
      const textarea = document.querySelector("textarea");
      this.tasks.push(`${textarea.value}`);
      textarea.value = '';
    },
  },
};
</script>

<style scoped src="../styles/ToDo.css"></style>
