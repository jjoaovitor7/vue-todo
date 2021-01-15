<template>
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap"
    rel="stylesheet"
  />
  <div>
    <textarea id="tarefaTextField"></textarea>
  </div>
</template>

<script>
export default {
  name: "TextArea",
}
</script>

<style scoped>
div {
  display: flex;
  height: 160px;
  width: 500px;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  background: #ffc107;
  padding: 15px 0;
}

textarea {
  border: none;
  border-radius: 15px;
  height: 75px;
  width: 250px;
  resize: none;
  padding: 15px;
  font-size: 16px;
  font-family: "Rock Salt", cursive;
}
</style>
