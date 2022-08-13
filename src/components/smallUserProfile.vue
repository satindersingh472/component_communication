<template>

    <div class="user_list">
        <button class="click_it" @click="send_to_parent">click this button</button>
        <h2>{{many_users[`name`]}}</h2>
        <h2>{{many_users[`age`]}}</h2>
        <p>{{many_users[`is_premium`]}}</p>
    </div>
</template>

<script>
    export default {
        methods: {
            send_to_parent() {
                this.$emit(`user_clicked`,this.many_users);
            }
        },
        props: {
            many_users: Object
        },        
    }
</script>

<style scoped>
template{
    display: grid;
    grid-auto-columns: 1fr 1fr 1fr;
}
.user_list{
    display: grid;
}
</style>