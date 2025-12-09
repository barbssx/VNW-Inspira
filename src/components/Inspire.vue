<template>
	<section class="inspire-section">
		<h1>Inspire-se</h1>
		<div class="cards-container">
			<Card v-for="i in img" :key="i.id" :img="i.download_url" />
		</div>
	</section>
</template>

<script setup>
import Card from "./Card.vue";
import { ref } from "vue";
import axios from "axios";

const img = ref([]);

async function getImagens() {
	const res = await axios.get("https://picsum.photos/v2/list?page=2&limit=100");
	img.value = res.data;
}

getImagens();
</script>

<style scoped>
.inspire-section {
	display: flex;
	flex-direction: column;
	h1 {
		margin-bottom: 4rem;
	}
}

.cards-container {
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	gap: 15px;
}

@media (max-width: 900px) {
	.cards-container {
		grid-template-columns: repeat(1, 1fr);
	}

	.inspire-section {
		margin: 0;
	}
}
</style>
