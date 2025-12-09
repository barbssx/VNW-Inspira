<template>
	<div class="card">
		<img :src="img" alt="Card image" />
		<Icon class="icon-heart" icon="line-md:heart-filled" width="24" height="24" />
	</div>
</template>

<script setup>
import { Icon } from "@iconify/vue";

defineProps(["img"]);
</script>

<style lang="scss" scoped>
.card {
	position: relative;
	width: 350px;
	height: 500px;

	img {
		width: 100%;
		height: 100%;
		border-radius: 15px;
		object-fit: cover;
	}

	.icon-heart {
		position: absolute;
		top: 20px;
		right: 20px;
		color: rgb(255, 255, 255);
		filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.3));
		cursor: pointer;
	}

	&:is(:hover, :focus) {
		box-shadow: 0px 8px 10px 1px rgba(0, 0, 0, 0.2);
		transform: translateY(-8px);
		border-radius: 15px;
	}
}

@media (max-width: 900px) {
	.card {
		width: 100%;

		margin: 0;
	}
}
</style>
