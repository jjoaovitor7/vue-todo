<template>
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Rock+Salt&display=swap"
    rel="stylesheet"
  />
  <div>
      <p>{{ task }}</p>
  </div>
</template>

<script>
export default {
  props: { task: String },
};
</script>

<style scoped>
div {
  background: #ffeb3b;
  display: flex;
  height: 160px;
  width: 500px;
  margin: 0 auto;
  justify-content: center;
  align-items: center;
  font-family: "Rock Salt", cursive;
}

header h1 {
  font-size: 72px;
}
</style>