<template>
	<section class="banner">
		<div class="banner-textos">
			<h1>Onde a paisagem vira <span class="pink-title">inspiração</span>.</h1>
			<h3>Explore paisagens, cores e luzes que inspiram novas histórias através da fotografia.</h3>
		</div>
		<img class="fotoBanner" :src="fotoBanner" alt="" />
	</section>
</template>
<script setup>
import fotoBanner from "../assets/fotografo.png";
</script>
<style scoped lang="scss">
.banner {
	display: flex;
	flex-direction: row;
	padding: 4rem;
}

.banner-textos {
	display: flex;
	flex-direction: column;
	justify-content: center;

	h1 {
		font-size: 70px;
		margin-bottom: 2rem;
	}

	&:hover,
	&:focus {
		color: var(--pink);
		transform: scale(1);
		transition-duration: 1s;
	}
}

.pink-title {
	color: var(--pink);
}

@media (max-width: 900px) {
	.banner {
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 1rem 2rem;
	}

	.banner-textos {
		text-align: center;
		margin: 1rem 0;
		width: 100%;

		h1 {
			font-size: 35px;
			line-height: 1.2;
		}

		h3 {
			font-size: 16px;
			line-height: 1.5;
		}
	}

	.fotoBanner {
		max-width: 100%;
		height: auto;
		margin-top: 1rem;
	}
}
</style>
