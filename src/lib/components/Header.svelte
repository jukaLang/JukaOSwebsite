<script>
	import Icon from '@iconify/svelte';
	import Button from './Button.svelte';
	import { onMount } from 'svelte';
	let isActive = false;
	let isScrolled = false;

	const handleScroll = () => {
		isScrolled = window.scrollY > 0;
	};

	onMount(() => {
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

<header class="header" class:scrolled={isScrolled}>
	<div class="header__container">
		<a href="/" class="header__container__logo">
			<img src="logo.svg" alt="JukaOS Logo" />
			Visual Juka OS
		</a>

		<button
			class="header__container__burger"
			class:active={isActive}
			on:click={() => (isActive = !isActive)}
		>
			<div class="header__container__burger__item"></div>
			<div class="header__container__burger__item"></div>
			<div class="header__container__burger__item"></div>
		</button>

		<nav class="header__container__nav" class:active={isActive}>
			<a href="/" class="header__container__nav__item">Home</a>
			<a href="/" class="header__container__nav__item">Features</a>
			<a href="/" class="header__container__nav__item">Team</a>
			<a href="/" class="header__container__nav__item">Documentation</a>
			<a href="/"><Button type="fill" placeholder="Download" /></a>
			<div class="header__container__nav__socials">
				<Icon icon="ic:baseline-discord" color="white" width="25" height="25" />
				<Icon icon="mdi:github" color="white" width="25" height="25" />
				<Icon icon="mdi:patreon" color="white" width="25" height="25" />
				<Icon icon="mdi:youtube" color="white" width="25" height="25" />
			</div>
		</nav>

		<div class="header__container__socials">
			<Icon icon="ic:baseline-discord" color="white" width="25" height="25" />
			<Icon icon="mdi:github" color="white" width="25" height="25" />
			<Icon icon="mdi:patreon" color="white" width="25" height="25" />
			<Icon icon="mdi:youtube" color="white" width="25" height="25" />
		</div>
	</div>
</header>

<style lang="scss">
	.header {
		@include container;

		& {
			height: 120px;
			background-color: transparent;
			position: fixed;
			width: 100%;
			z-index: 3;
			transition: ease-in-out 0.3s;

			&.scrolled {
				background-color: $bg-clr;
			}
		}

		&__container {
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			padding: 0 2rem;

			&__logo {
				color: white;
				display: flex;
				flex-direction: row;
				align-items: center;
				font-size: 1.2rem;
				font-weight: bold;
				gap: 12px;
			}

			&__socials {
				@media (max-width: $max-width) {
					display: none;
				}
			}

			&__burger {
				display: none;
				border: none;
				background-color: transparent;
				flex-direction: column;
				justify-content: space-between;
				width: 30px;
				height: 20px;
				cursor: pointer;
				z-index: 1;

				@media (max-width: 1080px) {
					display: flex;
				}

				&.active {
					.header__container__burger__item:nth-child(1) {
						transform: translateY(9px) rotate(45deg);
					}

					.header__container__burger__item:nth-child(2) {
						opacity: 0;
					}

					.header__container__burger__item:nth-child(3) {
						transform: translateY(-9px) rotate(-45deg);
					}

					.header__container__burger__item {
						background-color: black;
					}
				}

				&__item {
					background-color: white;
					width: 100%;
					height: 2px;
					transition:
						transform 0.3s ease,
						opacity 0.3s ease;
				}
			}

			&__nav {
				display: flex;
				flex-direction: row;
				align-items: center;
				gap: 1rem;
				color: white;

				&__item:hover {
					color: #e3e3e3;
					transition: ease-in-out 0.3s;
				}

				&.active {
					top: 0;
				}

				&__socials {
					display: none;

					@media (max-width: $max-width) {
						display: block;
					}
				}

				@media (max-width: 1080px) {
					left: 0;
					color: black;
					width: 100%;
					height: 100vh;
					display: flex;
					justify-content: center;
					flex-direction: column;
					background-color: white;
					position: absolute;
					top: -100vh;
					transition: ease-in-out 0.3s;
				}
			}
		}
	}
</style>
