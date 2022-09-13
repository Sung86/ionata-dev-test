<template>
	<main>
		<section>
			<span class="headline">DATA DRIVEN CREATIVE</span>
			<div class="title">
				Crafting human connection through digital experience
			</div>
			<div class="subtitle">
				Werk is a strategic design agency powered by data analytics, market
				research, and digital technology.
			</div>
			<button class="lets-talk-btn">Let's talk</button>
		</section>
		<img class="image" src="@/assets/images/rock-sea.jpg" alt="rock-sea" />
	</main>
</template>
<style scoped>
main {
	padding-left: clamp(10px, 15%, 280px);
	height: 100%;
}
section {
	padding-left: clamp(10px, 15%, 115px);
	padding-right: clamp(10px, 15%, 30px);
}
.headline {
	position: relative;
	color: #1a1a1f;
	font-size: clamp(0.5rem, -0.875rem + 8.333vw, 0.8rem);
	font-weight: bold;
}
.headline::before {
	content: '';
	display: block;
	width: 30px;
	height: 1.5px;
	background: #1a1a1f;
	left: -80px;
	top: 5px;
	position: absolute;
}
.title {
	font-size: clamp(1rem, -0.875rem + 8.333vw, 4rem);
	font-weight: bolder;
	max-width: 1000px;
	margin: 30px 0;
}
.subtitle {
	max-width: 450px;
	font-size: 1rem;
	color: #5f5f62;
}
.lets-talk-btn {
	background-color: #92927c;
	width: 130px;
	height: 42px;
	border: 0;
	font-weight: bold;
	margin: 40px 0;
	cursor: pointer;
	color: #000;
}
.lets-talk-btn:hover {
	opacity: 0.5;
}
.image {
	width: 100%;
	max-height: 570px;
	min-height: 200px;
	object-fit: cover;
	background-position: center;
}
@media screen and (max-width: 530px) {
	.headline::before {
		display: none;
	}
}
@media screen and (max-width: 400px) {
	main {
		padding-left: 10px;
	}
}
</style>
