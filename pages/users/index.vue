<template>
    <div>
        <!-- <input type="text" v-model="userId">
        <button @click="onLoadUser" >Load User</button> -->
        When we input id and press the btn, It will lead to inputted "id"
    </div>
</template>

<!-- We dont have to write router config file, we just have to name folders properly
     So by folders, we can route. Nuxt based on folders makes config automatically
-->

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
