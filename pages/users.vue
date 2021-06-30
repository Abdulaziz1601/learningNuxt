<template>
    <div>
        <input type="text" v-model="userId">
        <button @click="onLoadUser" >Load User</button>
        <!-- When we input id and press the btn, It will lead to inputted "id" -->
        <nuxt-child />
    </div>
</template>

<script>
export default{
    data() {
        return {
            userId: ''
        }
    },
    // It is done programmaticaly:
    methods: {
        onLoadUser() {
            // using simple vue router
            this.$router.push('/users/' + this.userId)
            // After btn clicked, id is passed here, and page is linked to "users/inputtedID"
        }
    }
}
</script>
