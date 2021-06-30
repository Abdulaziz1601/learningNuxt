<template>
    <!-- back of nuxt - routes based on vue notes so we can use vue - routes,-->
    <!-- $routes.params.id shows dynamic segments entered in this route -->
    <!-- Using dynamic parameters in route -->
    <h1>A single user, with ID: {{ $route.params.id }}</h1>

</template>

 <!-- Nuxt adds more properties, for example route validation -->
 <script>
export default {
    // special method that nuxt exectutes, before rendering route
    validate(data) {
        console.log(data)
        // return true
        // Page is loaded, if and only if id is equal to 1
        // return data.params.id == 1
        // we can validate with regex also
        return /^\d+$/.test(data.params.id) // so, if id is not a number It will give us an error
    }
}
</script>