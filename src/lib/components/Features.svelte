<script lang="ts">
	import Icon from '@iconify/svelte';
	import Saos from 'saos';
</script>

<section class="features">
	<div class="features__container">
		<Saos animation={'fade-in .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
			<div class="features__container__header">
				<h2 class="features__container__header__title">Discover the Possibilities</h2>
				<p class="features__container__header__subtitle">Taking your Trimui beyond the limits!</p>
			</div>
		</Saos>
		<Saos animation={'from-left .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
			<img
				class="features__container__image"
				src="trimui.webp"
				alt="Trimui Handheld"
				width="600"
				height="260"
			/>
		</Saos>

		<ul class="features__container__list">
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<li class="features__container__list__item">
					<Icon icon="material-symbols:speed" width="60" height="60" color="#00E0BC" />
					<h3 class="features__container__list__item__title">Blazing Performance</h3>
					<p class="features__container__list__item__text">
						Enjoy lightning-fast load times and seamless multitasking, optimized specifically for
						your Trimui Smart Pro.
					</p>
				</li>
			</Saos>
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<li class="features__container__list__item">
					<Icon icon="mdi:art" width="60" height="60" color="#00E0BC" />
					<h3 class="features__container__list__item__title">Total Customization</h3>
					<p class="features__container__list__item__text">
						Tailor your device to match your style with customizable themes, wallpapers, and
						user-friendly layouts.
					</p>
				</li>
			</Saos>
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<li class="features__container__list__item">
					<Icon icon="mdi:controller" width="60" height="60" color="#00E0BC" />
					<h3 class="features__container__list__item__title">Enhanced Gaming</h3>
					<p class="features__container__list__item__text">
						Dive into an unparalleled gaming experience with game optimization and robust controller
						support built-in.
					</p>
				</li>
			</Saos>
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<li class="features__container__list__item">
					<Icon icon="mdi:security" width="60" height="60" color="#00E0BC" />
					<h3 class="features__container__list__item__title">Robust Security</h3>
					<p class="features__container__list__item__text">
						Keep your data secure with advanced security features and privacy controls, ensuring
						peace of mind.
					</p>
				</li>
			</Saos>
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<li class="features__container__list__item">
					<Icon icon="mdi:wifi" width="60" height="60" color="#00E0BC" />
					<h3 class="features__container__list__item__title">Stay Connected</h3>
					<p class="features__container__list__item__text">
						Connect effortlessly to Wi-Fi, Bluetooth, and cloud services for smooth data sharing and
						connectivity.
					</p>
				</li>
			</Saos>
		</ul>
	</div>
</section>

<style lang="scss">
	.features {
		@include container;

		& {
			position: relative;
			background-position: center;
			background-repeat: no-repeat;
			background-size: cover;

			&__container {
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: center;
				color: white;
				padding: 64px 32px;

				&__header {
					display: flex;
					flex-direction: column;
					align-items: center;
					justify-content: center;
					margin-bottom: 42px;
					text-align: center;

					&__subtitle {
						color: $primary-clr;
					}
				}

				&__image {
					filter: drop-shadow(0px 5px 10px rgba(0, 0, 0, 0.4));
					margin-bottom: 42px;
					width: 100%;
					max-width: 600px;
					height: auto;
				}

				&__list {
					list-style: none;
					display: flex;
					flex-direction: row;
					align-items: center;
					justify-content: center;
					row-gap: 46px;
					column-gap: 32px;
					flex-wrap: wrap;

					&__item {
						max-width: 310px;
						display: flex;
						flex-direction: column;
						align-items: center;
						text-align: center;

						&__title {
							color: $primary-clr;
							margin-bottom: 8px;
						}

						&__text {
							font-weight: 400;
						}
					}
				}
			}

			&:after {
				content: '';
				display: block;
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				z-index: -1;
				background: linear-gradient(180deg, #242526 0%, rgba(44, 45, 55, 0) 50%, #242526 100%);
			}

			&:before {
				content: '';
				display: block;
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				background-image: url(/features.webp);
				background-position: center;
				background-repeat: no-repeat;
				background-size: cover;
				filter: saturate(0);
				opacity: 0.1;
				pointer-events: none;
				z-index: -1;
			}
		}
	}
</style>
