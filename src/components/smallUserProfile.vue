<template>
    <div class="user_list">
        <h2>{{many_users[`name`]}}</h2>
        <h2>{{many_users[`age`]}}</h2>
        <p>{{many_users[`is_premium`]}}</p>
    </div>
</template>

<script>
    export default {
        props: {
            many_users: Object
        },        
    }
</script>

<style scoped>

</style>