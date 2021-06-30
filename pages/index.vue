<template>
	<section class="container">
		<!-- It relaods and goes to another page, but we wanna use it like SPA -->
		<!-- <a href="/users">Users</a> -->
		<!-- In vue we had to use router-link -->
		<!-- <router-link></router-link> -->
		<!-- In nuxt equivalent is nuxt-link -->
		<!-- "to" property states, where to link, after click -->
		<nuxt-link to="/users">Users</nuxt-link>

		<!-- Difference between COMPONENTS and PAGES -->
		<!-- PAGES are routes, using router, where we can visit -->
		<!-- COMPONENTS are building blocks of our app	`  -->
	</section>
</template>

<script>
	export default {}
</script>
