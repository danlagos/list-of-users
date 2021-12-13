<template>
  <div>
    <AddUser @user-info="addUserInfo" />
  </div>
</template>

<script>
// @ is an alias to /src
import AddUser from "@/components/AddUser.vue";

export default {
  name: "Users",
  components: {
    AddUser,
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
