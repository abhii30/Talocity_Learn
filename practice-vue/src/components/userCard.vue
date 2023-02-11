<script>
export default {
  props: {
    name: {
      type: String,
      default: "Abhishek",
    },
    roll: {
      type: String,
      default: 1201,
    },
  },
};
</script>

<template>
  <div>
    <h1>User :{{ name }}</h1>
    <h2>Roll :{{ roll }}</h2>
  </div>
</template>

<style></style>
