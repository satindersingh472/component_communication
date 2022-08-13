<template>
  <div id="app">
    <small-user-profile v-for="(user,index) in users" :key="index" :many_users="user"></small-user-profile>
  </div>
</template>

<script>
import SmallUserProfile from "@/components/smallUserProfile.vue";
export default {
  name: "App",
  components: {
    SmallUserProfile,
  },
  data() {
    return {
      users: [
        {
          name: `name_one`,
          age: 7,
          is_premium: false,
          
        },
        {
          name: `name_two`,
          age: 10,
          is_premium: true,
          
        },
        {
          name: `name_three`,
          age: 9,
          is_premium: false,
          
        }
      ]
    };
  }
};
</script>

<style></style>
