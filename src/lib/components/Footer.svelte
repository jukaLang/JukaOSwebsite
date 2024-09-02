<footer class="footer">
	<div class="footer__container">
		<div class="footer__container__header">
			<ul class="footer__container__header__list">
				<li class="footer__container__header__list__item--title">Menu</li>
				<li class="footer__container__header__list__item"><a href="/">Home</a></li>
				<li class="footer__container__header__list__item"><a href="#features">Features</a></li>
				<li class="footer__container__header__list__item"><a href="#about">About</a></li>
				<li class="footer__container__header__list__item"><a href="#faq">FAQ</a></li>
			</ul>
			<ul class="footer__container__header__list">
				<li class="footer__container__header__list__item--title">Community</li>
				<li class="footer__container__header__list__item">
					<a href="https://discord.gg/hjmCcrbD">Discord</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://twitter.com/jukaLang">Twitter</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://www.facebook.com/jukalang/">Facebook</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://www.youtube.com/@jukalang">Youtube</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://www.instagram.com/jukalanguage/">Instagram</a>
				</li>
			</ul>
			<ul class="footer__container__header__list">
				<li class="footer__container__header__list__item--title">More</li>
				<li class="footer__container__header__list__item">
					<a href="https://jukalang.com/donate">Donate</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://jukalang.com/privacy">Privacy</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://jukalang.com/license">License</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://jukalang.com/contact">Contact Us</a>
				</li>
				<li class="footer__container__header__list__item">
					<a href="https://github.com/jukaLang/juka">Github Source</a>
				</li>
			</ul>
		</div>
		<div class="footer__container__copy">
			<p>Copyright © 2024 Visual Juka OS</p>
		</div>
	</div>
</footer>

<style lang="scss">
	.footer {
		@include container;

		& {
			background-color: $secondary-clr;
		}

		&__container {
			display: flex;
			flex-direction: column;
			padding: 32px;
			gap: 32px;

			&__copy {
				display: flex;
				align-items: center;
				color: white;
				justify-content: center;
			}

			&__header {
				display: flex;
				flex-direction: row;
				justify-content: space-around;
				align-items: center;
				flex-wrap: wrap;
				gap: 32px;

				&__list {
					display: flex;
					list-style: none;
					flex-direction: column;
					align-items: flex-start;

					&__item {
						color: white;

						&--title {
							color: white;
							font-size: clamp(1rem, 0.9388rem + 0.3265vw, 1.2rem);
							margin-bottom: 12px;
						}
					}
				}
			}
		}
	}
</style>
