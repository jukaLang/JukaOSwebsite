<script>
	import Icon from '@iconify/svelte';
	import Saos from 'saos';
</script>

<section class="about">
	<div class="about__container">
		<Saos animation={'fade-in .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
			<div class="about__container__header">
				<h2 class="about__container__header__title">What is Visual Juka OS?</h2>
				<p class="about__container__header__subtitle">Enhance Your TSP Experience</p>

				<p class="about__container__header__text">
					Juka OS powers the Trimui Smart Pro, so you get a seamless gaming experience right from
					the start. It works effortlessly, and it includes all the features and tools every gamer
					needs. Moreover, you can jump into your games without any hassle. In addition, Juka OS
					offers an intuitive design, making it easy to navigate. As a result, you spend less time
					setting up and more time enjoying your games.
				</p>
			</div>
		</Saos>
		<div class="about__container__features">
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<article class="about__container__features__article">
					<h3 class="about__container__features__article__title">
						<Icon icon="ant-design:android-filled" width="20" height="20" color="#00E0BC" /> Android
						Based
					</h3>
					<p class="about__container__features__article__text">
						Built on Android, this OS works with many apps and gives great performance. So, it makes
						your Trimui gaming experience smooth and easy. Plus, you can enjoy a wide range of games
						without any hassle.
					</p>
				</article>
			</Saos>
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<article class="about__container__features__article">
					<h3 class="about__container__features__article__title">
						<Icon icon="ph:code-bold" width="20" height="20" color="#00E0BC" /> Open Source
					</h3>
					<p class="about__container__features__article__text">
						The OS is open-source, so it lets everyone join in. You can contribute, customize, and
						create new features. This way, the whole community can innovate and grow together.
					</p>
				</article>
			</Saos>
			<Saos animation={'from-bottom .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
				<article class="about__container__features__article">
					<h3 class="about__container__features__article__title">
						<Icon icon="fluent:people-community-32-filled" width="20" height="20" color="#00E0BC" />
						Community-Centric
					</h3>
					<p class="about__container__features__article__text">
						This OS focuses on teamwork. It lets everyone join in and make it better. So, the
						community can shape and improve the experience together.
					</p>
				</article>
			</Saos>
		</div>
	</div>
</section>

<style lang="scss">
	.about {
		@include container;

		&__container {
			display: flex;
			flex-direction: column;
			padding: 64px 32px;

			&__header {
				display: flex;
				flex-direction: column;
				align-items: center;
				color: white;
				margin-bottom: 32px;

				&__subtitle {
					color: $primary-clr;
					margin-bottom: 32px;
				}

				&__text {
					text-align: center;
				}
			}
			&__features {
				display: flex;
				flex-direction: row;
				justify-content: center;
				flex-wrap: wrap;
				column-gap: 44px;
				row-gap: 32px;

				&__article {
					flex: 1;
					max-width: 360px;
					min-width: 280px;
					color: white;
					display: flex;
					flex-direction: column;
					gap: 10px;

					&__title {
						display: flex;
						align-items: center;
						gap: 8px;
						font-size: 16px;
					}
				}
			}
		}
	}
</style>
