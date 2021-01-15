<template>
  <div id="page-home">
    <Header />
    <TextArea />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap"
      rel="stylesheet"
    />

    <button @click="addTask" id="btn-ok">Ok</button>
    <Task task="" />
    {{ tasks }}
  </div>
</template>

<script>
import Header from "../components/Header";
import TextArea from "../components/TextArea";
import Task from "../components/Task";
import { compile } from "vue";

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
    Task,
  },
  methods: {
    addTask() {
      // view model
      // const vm = this;
      const textarea = document.querySelector("textarea");
      this.tasks.push(compile(<Task task={textarea.value} />));
      console.log(this.tasks);
    },
  },
};
</script>

<style scoped>
div {
  width: 550px;
  height: 600px;
  overflow: scroll;
  margin-top: -15px;
}
</style>