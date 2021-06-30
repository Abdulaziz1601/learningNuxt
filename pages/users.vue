<template>
    <!-- So this file is a wrapper fro index file, and user folder,-->
    <!--and other files, that we wanna load -->
    <!-- If we wanna use Id input and btn, in nested files, we have to copy IT here -->
    <div>
        <div class="input-wrapper">
            <input type="text" v-model="userId">
            <button @click="onLoadUser" >Load User</button>
        </div>
        <!-- THen we add special component -->
        <nuxt-child />
        <!-- it simply marks the place where different sections of route are loaded -->
        <!-- So we it shows input and btn, and child of users index file, which has text -->
        <!-- So after writing any ID, loads any Id and injects it into nuxtChild and shows It -->
        <!-- So, it is a nested route that we nest the content should be rendered into another page   -->
        <!-- This usage is optional, when we have sub-routes in a wrapper, that should be changed in the same page -->
    </div>
</template>


<!-- Script also is copied  -->
<script>
    export default {
        // If we wanna use users-header layout
        layout: 'users',
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
        },
        
        // It looks for layout folder for users, If it finds It.
        // It uses users layout instead of default one
    
}
</script>
