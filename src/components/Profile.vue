<template>
    <div>
        <h2>Profile for user {{userProfile}}</h2>
    </div>
</template>
<script>
export default {
    data() {
        return {
            userProfile: this.$route.params.user_id
        }
    },
    methods: {
        updateId(){
            this.userProfile = this.$route.params.user_id
        }
    },
    watch: {
        $route: 'updateId'
    }
}
</script>
<style scoped>
h2 {
    text-decoration-line: underline
}
</style>