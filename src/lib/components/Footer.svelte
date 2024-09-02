<footer class="footer">
	<div class="footer__container">
		<div class="footer__container__header">
			<ul class="footer__container__header__list">
				<li class="footer__container__header__list__item--title">Menu</li>
				<li class="footer__container__header__list__item">Home</li>
				<li class="footer__container__header__list__item">Features</li>
				<li class="footer__container__header__list__item">Team</li>
				<li class="footer__container__header__list__item">Documentation</li>
			</ul>
			<ul class="footer__container__header__list">
				<li class="footer__container__header__list__item--title">Community</li>
				<li class="footer__container__header__list__item">Discord</li>
				<li class="footer__container__header__list__item">Twitter</li>
				<li class="footer__container__header__list__item">Facebook</li>
				<li class="footer__container__header__list__item">Youtube</li>
				<li class="footer__container__header__list__item">Instagram</li>
			</ul>
			<ul class="footer__container__header__list">
				<li class="footer__container__header__list__item--title">More</li>
				<li class="footer__container__header__list__item">Donate</li>
				<li class="footer__container__header__list__item">Privacy</li>
				<li class="footer__container__header__list__item">License</li>
				<li class="footer__container__header__list__item">Contact Us</li>
				<li class="footer__container__header__list__item">Github Source</li>
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
