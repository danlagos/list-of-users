<template>
  <div>
    <form @submit.prevent="onSubmit">
      <label for="name">name</label>
      <input v-model="name" id="name" type="text" />
      <label for="age">Age</label>
      <input v-model.number="age" id="age" type="number" />
      <button type="submit" value="Submit">Add User</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "AddUserForm",
  data() {
    return {
      name: "",
      age: "",
      key: null,
    };
  },
  methods: {
    onSubmit() {
      let userPayload = {
        name: this.name,
        age: this.age,
        key: Math.random() * (100 - 1) + 100,
      };
      this.$emit("user-info", userPayload);
      this.name = "";
      this.age = "";
      this.key = null;
    },
  },
};
</script>

<style scoped></style>
