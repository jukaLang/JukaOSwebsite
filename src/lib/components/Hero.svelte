<script>
	import About from './About.svelte';
	import Button from './Button.svelte';
</script>

<section class="hero">
	<div class="hero__container">
		<h1 class="hero__container__title">
			Juka OS, the <br /> <span class="hero__container__title__highlight"> gamer's choice.</span>
		</h1>
		<p class="hero__container__text">
			Visual Juka OS is a custom-built operating system designed specifically for the Trimui Smart
			Pro. Crafted by gamers for gamers, it offers a seamless, high-performance experience. Juka OS
			is under continuous development by a passionate community, ensuring you get the best out of
			your gaming device.
		</p>
		<div class="hero__container__wrapper">
			<a href="https://github.com/jukaLang" target="_blank"
				><Button placeholder="Try vJuka OS" type="fill" /></a
			>
			<a href="https://www.patreon.com/jukalang" target="_blank"
				><Button placeholder="Join Us On Patreon" type="border" /></a
			>
		</div>
	</div>
</section>

<style lang="scss">
	.hero {
		@include container;

		& {
			background: linear-gradient(180deg, rgba(36, 37, 38, 0) 0%, #242526 100%), url(/banner.webp);
			background-position: center;
			background-repeat: no-repeat;
			background-size: cover;
			height: 100vh;
		}

		&__container {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			color: white;
			text-align: center;
			padding: 0 16px;

			&__title {
				line-height: 1;
				margin-bottom: 16px;

				&__highlight {
					color: $primary-clr;
				}
			}

			&__text {
				margin-bottom: 22px;
				max-width: 800px;
			}

			&__wrapper {
				display: flex;
				flex-direction: row;
				gap: 12px;
				flex-wrap: wrap;
				justify-content: center;
			}
		}
	}
</style>
