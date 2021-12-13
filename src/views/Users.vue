<template>
  <div>
    <AddUser @user-info="addUserInfo" />
    <UserList v-for="(user, index) in userData" :key="index" />
  </div>
</template>

<script>
// @ is an alias to /src
import AddUser from "@/components/AddUser.vue";
import UserList from "@/components/UserList.vue";

export default {
  name: "Users",
  components: {
    AddUser,
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
