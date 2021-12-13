<template>
  <div>
    <form @submit.prevent="submitHandler">
      <label for="username">Username</label>
      <input id="username" type="text" />
      <label for="age">Age</label>
      <input id="age" type="number" />
    </form>
  </div>
</template>

<script>
export default {
  name: "AddUser",
};
</script>

<style scoped></style>
