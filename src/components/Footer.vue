<template>
	<footer>
		<div class="listas-footer">
			<ul>
				<h3>Contato</h3>
				<li>contato@inspiralens.com</li>
				<li>Central de ajuda</li>
				<li>Rio de Janeiro – Brasil</li>
			</ul>
			<ul>
				<h3>Sobre</h3>
				<li>Politicas</li>
				<li>Politicas de privacidade</li>
				<li>Blog</li>
			</ul>
			<div class="newsletter">
				<h3>Assine nossa newsletter</h3>
				<input type="email" placeholder="Digite seu email" />
				<button class="btn-submit" type="submit">Inscrever-se</button>
			</div>
		</div>

		<div class="redes-sociais">
			<img src="./assets/Facebook.png" alt="" />
			<img src="./assets/Twitter.png" alt="" />
			<img src="./assets/Instagram.png" alt="" />
			<img src="./assets/LinkedIn.png" alt="" />
		</div>
	</footer>
</template>

<script setup></script>

<style lang="scss" scoped>
.listas-footer {
	display: flex;
	gap: 10px;
	justify-content: space-evenly;

	ul {
		list-style: none;
		font-size: 18px;

		li {
			margin-bottom: 8px;
			cursor: pointer;

			&:hover {
				text-decoration: underline;
			}
		}
	}

	h3 {
		margin-bottom: 10px;
	}
}

.newsletter {
	display: flex;
	flex-direction: column;
	justify-content: center;

	input {
		padding: 8px;
	}

	.btn-submit {
		margin-top: 10px;
		background-color: var(--pink);
		border: none;
		padding: 8px 12px;
		color: white;
		border-radius: 5px;
		cursor: pointer;

		&:hover {
			transform: scale(1.05);
		}
	}
}

@media (max-width: 900px) {
	.listas-footer {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
	}

	.newsletter {
		margin-top: 20px;
		width: 100%;

		input {
			width: 80%;
			margin: 0 auto;
		}

		.btn-submit {
			width: 50%;
			margin: 10px auto 0 auto;
		}
	}
}
</style>
