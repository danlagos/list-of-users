<template>
  <h1>User List</h1>
  <p>User: {{ this.user.name }}</p>
  <p>Age: {{ this.user.age }}</p>
</template>

<script>
export default {
  name: "UserList",
  props: {
    user: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped></style>
