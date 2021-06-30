<template>
    <div>
        <!-- <input type="text" v-model="userId">
        <button @click="onLoadUser" >Load User</button> -->
        <!-- When we input id and press the btn, It will lead to inputted "id" -->

        <!-- We wanna load userId right below, the input button, on "/users" page-->
        <!-- We have to create new file next to users folder, next to the folder,-->
        <!-- Where we wanna create nested routing, newly created file has to have -->
        <!-- same name, as the folder "users.vue" -->

        <!-- So we made wrapper, users.vue  -->
        <div>
            <!-- <Header /> -->
            <p>Please enter the ID and click the button</p>
        </div>
        <!-- So this will be replaced, by user.vue file once it is submitted -->
    </div>
</template>

<!-- We dont have to write router config file, we just have to name folders properly
     So by folders, we can route. Nuxt based on folders makes config automatically
-->

<script>
// import Header from '@/components/Header'

export default{
    // components: {
			// Header
		// },
//     data() {
//         return {
//             userId: ''
//         }
//     },
//     // It is done programmaticaly:
//     methods: {
//         onLoadUser() {
//             // using simple vue router
//             this.$router.push('/users/' + this.userId)
//             // After btn clicked, id is passed here, and page is linked to "users/inputtedID"
//         }
//     }
    layout: 'users'

}
</script>
