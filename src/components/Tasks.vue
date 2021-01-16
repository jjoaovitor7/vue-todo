<template>
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap"
    rel="stylesheet"
  />

  <div id="button-addTask">
    <button @click="addTask" id="btn-ok">Ok</button>
  </div>
  <div class="tasks" v-for="(task, index) in tasks" :key="index">
    {{ task }}
    <!-- <input type="checkbox" /> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      tasks: [],
    };
  },
  methods: {
    addTask() {
      // view model // const vm = this;

      const textarea = document.querySelector("textarea");

      if (textarea.value === "") {
        this.$toast.show("O campo de tarefa não pode ser vazio.", {
          type: "error",
          duration: 5000,
        });
        return 0;
      }

      if (textarea.value.length < 8) {
        this.$toast.show(
          "O campo de tarefa não pode ter menos que 8 caracteres",
          {
            type: "error",
            duration: 5000,
          }
        );
        return 0;
      }

      this.tasks.push(`${textarea.value}`);
      textarea.value = "";
    },
  },
};
</script>

<style scoped src="../styles/Tasks.css"></style>