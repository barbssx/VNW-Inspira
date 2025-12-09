<template>
	<header>
		<div class="logo-titulo">
			<img :src="logo" alt="" />
			<h1>Inspira</h1>
		</div>
		<nav>
			<ul>
				<li>
					<a href=""><Icon icon="line-md:search" width="24" height="24" /></a>
				</li>
				<li><a href="">Inicio</a></li>
				<li><a href="">Galeria</a></li>
				<li><a href="">Favoritos</a></li>
				<li>
					<a href=""><Icon icon="line-md:account" width="24" height="24" /> </a>
				</li>
			</ul>
		</nav>
	</header>
</template>

<script setup>
import { Icon } from "@iconify/vue";
import logo from "../assets/logo.svg";
</script>

<style scoped>
header {
	display: flex;
	justify-content: space-between;
	margin: 2rem;
}

.logo-titulo {
	display: flex;
	flex-direction: row;
	gap: 1rem;
	align-items: center;
}

nav ul {
	display: flex;
	text-decoration: none;

	li {
		list-style: none;
		margin: 0 2rem;
		font-size: 18px;

		a {
			text-decoration: none;
			color: inherit;
		}

		&:hover {
			background-color: black;
			border-radius: 15px;
			color: white;
			padding: 5px 10px;
		}
	}
}

@media (max-width: 900px) {
	header {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 1rem;
	}

	nav ul {
		margin-top: 1rem;
		flex-wrap: wrap;
		justify-content: center;
		li {
			margin: 0.5rem;
			font-size: 16px;
		}
	}
}
</style>
