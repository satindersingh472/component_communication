<template>
  <div id="app">
    <small-user-profile v-for="user in users" :key="user[`id`]" :many_users="user" @user_clicked="show_username"></small-user-profile>
      <h1 v-if="chosen_usernames !== undefined"> name is: {{chosen_usernames[`name`]}}</h1>
      <p v-if="chosen_usernames !== undefined" >age is: {{chosen_usernames[`age`]}}</p>
      <p v-else-if="chosen_usernames === undefined" >Click the buttons to see data here</p>
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
