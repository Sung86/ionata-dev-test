<template>
	<header>
		<img
			src="@/assets/images/logos/werk.svg"
			alt="logo"
			width="80"
			height="80"
		/>
		<div class="nav-container1">
			<ol class="nav">
				<li>Service</li>
				<li>Product</li>
				<li>About</li>
				<li>Blog</li>
				<li>Career</li>
			</ol>
			<button class="get-started-btn">Get started</button>
		</div>
		<div class="nav-container2">
			<img
				v-if="!isOpenSideMenu"
				class="burger-bar-icon"
				src="@/assets/images/burger-bar.webp"
				alt="burger bar"
				width="50"
				height="50"
				@click="onToggleSideMenu"
			/>
			<img
				v-else
				class="close-icon"
				src="@/assets/images/close.webp"
				alt="close"
				width="30"
				height="30"
				@click="onToggleSideMenu"
			/>
		</div>
	</header>
</template>

<script>
export default {
	props: {
		isOpenSideMenu: {
			type: Boolean,
			default: false,
		},
	},
	emits: ['toggleSideMenu'],
	methods: {
		onToggleSideMenu() {
			this.$emit('toggleSideMenu');
		},
	},
};
</script>

<style scoped>
header {
	display: flex;
	align-items: center;
	justify-content: space-between;
	padding-top: 15px;
	padding-bottom: 60px;
	padding-left: clamp(10px, 15%, 62px);
	padding-right: clamp(10px, 5%, 62px);
}
.nav-container1 {
	display: flex;
	justify-content: space-between;
	min-width: 650px;
	font-weight: bold;
}
.nav {
	display: flex;
	list-style: none;
	justify-content: space-around;
	width: 100%;
	margin-right: 20px;
}
.nav li {
	cursor: pointer;
}
.get-started-btn {
	background-color: #42491c;
	color: #fff;
	min-width: 175px;
	height: 52px;
	border: none;
	cursor: pointer;
	font-weight: bold;
}
.get-started-btn:hover {
	opacity: 0.5;
}
.nav-container2 {
	display: none;
}
.burger-bar-icon {
	cursor: pointer;
}
.close-icon {
	cursor: pointer;
}
@media screen and (max-width: 820px) {
	.nav-container1 {
		display: none;
		min-width: auto;
	}
	.nav-container2 {
		display: block;
	}
}
</style>
