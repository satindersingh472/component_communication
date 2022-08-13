<template>
  <div id="app">
    <small-user-profile v-for="user in users" :key="user[`id`]" :many_users="user"></small-user-profile>
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
          id: 101
          
        },
        {
          name: `name_two`,
          age: 10,
          is_premium: true,
          id:201
        },
        {
          name: `name_three`,
          age: 9,
          is_premium: false,
          id:301
        }
      ]
    };
  }
};
</script>

<style></style>
