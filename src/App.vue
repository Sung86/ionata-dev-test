<template>
	<Header :isOpenSideMenu="isOpenSideMenu" @toggleSideMenu="toggleSideMenu" />
	<div
		class="sidebar-container"
		:style="{ width: isOpenSideMenu ? '100vw' : '0' }"
	>
		<Sidebar :isOpenSideMenu="isOpenSideMenu" />
	</div>
	<Landing />
</template>
<script>
import { defineAsyncComponent } from 'vue';
export default {
	components: {
		Header: defineAsyncComponent(() => import('@/components/Header')),
		Sidebar: defineAsyncComponent(() => import('@/components/Sidebar')),
		Landing: defineAsyncComponent(() => import('@/views/Landing')),
	},
	data: () => ({
		isOpenSideMenu: false,
	}),
	methods: {
		toggleSideMenu() {
			this.isOpenSideMenu = !this.isOpenSideMenu;
		},
	},
};
</script>
<style scoped>
.sidebar-container {
	background-color: #fff;
	height: 100vh;
	width: 0;
	position: absolute;
	right: 0;
	z-index: 1000;
	transition: width ease-in-out 0.4s;
}
</style>
<style>
@import url('https://fonts.googleapis.com/css2?family=Work+Sans:wght@100;200;400&display=swap');
* {
	font-family: 'Work Sans', sans-serif;
}
html,
body {
	margin: 0;
	padding: 0;
	height: 100vh;
}
@media screen and (min-width: 820px) {
	.sidebar-container {
		display: none;
	}
}
</style>
