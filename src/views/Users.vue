<template>
  <div>
    <AddUserForm @user-info="addUserInfo" />
    <UserList v-for="(user, index) in userData" :key="index" />
  </div>
</template>

<script>
// @ is an alias to /src
import AddUserForm from "@/components/AddUserForm.vue";
import UserList from "@/components/UserList.vue";

export default {
  name: "Users",
  components: {
    AddUserForm,
    UserList,
  },
  data() {
    return {
      userData: [],
    };
  },
  methods: {
    addUserInfo(userPayload) {
      this.userData.push(userPayload);
      console.log(`user: ${this.userData}`);
    },
  },
};
</script>
