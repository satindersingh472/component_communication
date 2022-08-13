<template>
  <div id="app">
    <small-user-profile v-for="user in users" :key="user[`id`]" :many_users="user" @user_clicked="show_username"></small-user-profile>
  </div>
</template>

<script>
import SmallUserProfile from "@/components/smallUserProfile.vue";
export default {
  name: "App",
  components: {
    SmallUserProfile,
  },
  methods: {
    show_username(many_users) {
      this.chosen_usernames = many_users;
    }
  },
  data() {
    return {
      chosen_usernames: undefined,
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
