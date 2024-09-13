<template>
	<!-- [Хедер]: Хедер -->
	<header class="header">
		<div class="container">

			<!-- [Хедер]: Навигация -->
			<ul class="nav">

				<!-- [Хедер]: Навигация -->
				<li v-for="item in navList" :key="item.id">
					<RouterLink :to="item.link"> {{ item.title }} </RouterLink>
				</li>

			</ul>

		</div>
	</header>
</template>

<script setup>
import { ref } from "vue"
import { RouterLink } from "vue-router";

const navList = ref([
	{
		id: 0,
		link: "/",
		title: "Home",
	},
	{
		id: 1,
		link: "/todo",
		title: "Todo",
	},
	{
		id: 2,
		link: "/advices",
		title: "Advices",
	},
	{
		id: 3,
		link: "/calculator",
		title: "Calculator",
	},
	{
		id: 4,
		link: "/register",
		title: "Register",
	},
])
</script>

<style>
.header {
	padding: 32px 0;
}

.nav {
	display: flex;
	align-items: center;
	justify-content: center;
	gap: 20px;
}

.nav a {
	font-size: 24px;
	color: var(--green-text-color);
	transition: var(--main-transition);
}

.nav li:hover a:not(.router-link-exact-active) {
	background: var(--dark-grey-color);
}

.nav li a.router-link-exact-active {
	color: var(--grey-text-color);
}

</style>