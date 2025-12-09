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
			<img :src="Facebook" alt="Facebook" />
			<img :src="Twitter" alt="Twitter" />
			<img :src="Instagram" alt="Instagram" />
			<img :src="LinkedIn" alt="LinkedIn" />
		</div>
	</footer>
</template>

<script setup>
import Facebook from "../assets/Facebook.png";
import Twitter from "../assets/Twitter.png";
import Instagram from "../assets/Instagram.png";
import LinkedIn from "../assets/LinkedIn.png";
</script>

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

.redes-sociais {
	padding: 0% 2rem 2rem 2rem;
	display: flex;
	justify-content: center;
	gap: 20px;
	margin-top: 20px;

	img {
		width: 30px;
		height: 30px;
		cursor: pointer;

		&:hover {
			transform: scale(1.2);
		}
	}
}
</style>
