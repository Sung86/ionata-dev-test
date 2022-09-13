<template>
	<aside
		class="sidebar"
		:style="{ display: isOpenSideMenu ? 'block' : 'none' }"
	>
		<ol class="nav">
			<li>Service</li>
			<li>Product</li>
			<li>About</li>
			<li>Blog</li>
			<li>Career</li>
		</ol>
	</aside>
</template>

<script>
export default {
	props: {
		isOpenSideMenu: {
			type: Boolean,
			default: false,
		},
	},
};
</script>

<style scoped>
.sidebar {
	height: 100%;
	transition: all ease-in-out 0.5s;
}
.nav {
	display: flex;
	flex-direction: column;
	list-style: none;
	align-items: center;
	margin-right: 20px;
}
.nav li {
	cursor: pointer;
	font-size: 50px;
	margin-bottom: 20px;
}
.nav li:hover {
	padding-bottom: 10px;
	border-bottom: 5px solid #000;
	line-height: 48px;
}
</style>
