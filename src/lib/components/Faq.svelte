<script lang="ts">
	import Icon from '@iconify/svelte';
	import Saos from 'saos';
	import { fade, slide } from 'svelte/transition';

	type FAQItem = {
		question: string;
		answer: string;
		isOpen: boolean;
	};

	let faqs: FAQItem[] = [
		{
			question: 'Where does Visual Juka OS run?',
			answer:
				"Visual Juka OS is a special system for the Trimui Smart Pro (TSP). It uses Java to let you run Android apps on your TSP. This means you can do more with your handheld game device. Now, you can use many new apps that weren't available before.",
			isOpen: true
		},
		{
			question: 'How to contribute to the Project?',
			answer:
				'You can help improve Visual Juka OS by contributing to our project on Github. Join our community, share your ideas, and collaborate on code. Every contribution makes a difference!',
			isOpen: false
		},
		{
			question: 'How to Install Visual Juka OS?',
			answer:
				"Follow our step-by-step guide to install Visual Juka OS on our Github. Download the installation files, and follow the instructions. It's quick and easy!",
			isOpen: false
		},
		{
			question: 'I want help with Visual Juka OS. How can i do that?',
			answer:
				"If you need help with Visual Juka OS, open a github issue. You can find guides, FAQs, and contact options there. We're here to assist you!",
			isOpen: false
		}
	];

	const toggleFAQ = (index: number) => {
		faqs = faqs.map((faq, i) => ({
			...faq,
			isOpen: i === index ? !faq.isOpen : false
		}));
	};
</script>

<section class="faq">
	<div class="faq__container">
		<Saos animation={'fade-in .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
			<div class="faq__container__header">
				<h2 class="faq__container__header__title">Need More Info?</h2>
				<p class="faq__container__header__subtitle">Your TSP questions, answered.</p>
			</div>
		</Saos>

		<div class="faq__container__questions">
			{#each faqs as faq, index}
				<Saos animation={'from-left .8s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}>
					<div class="faq__container__questions__details">
						<div
							class="faq__container__questions__details__header"
							on:click={() => toggleFAQ(index)}
							role="button"
							aria-expanded={faq.isOpen}
							tabindex="0"
							on:keydown={(event) =>
								event.key === 'Enter' || event.key === ' ' ? toggleFAQ(index) : null}
						>
							<h3 class="faq__container__questions__details__header__summary">{faq.question}</h3>

							{#if !faq.isOpen}
								<Icon icon="ic:baseline-plus" width="25" height="25" />
							{:else}
								<Icon icon="ic:baseline-minus" width="25" height="25" />
							{/if}
						</div>
						{#if faq.isOpen}
							<p
								class="faq__container__questions__details__text"
								role="region"
								aria-hidden={!faq.isOpen}
								transition:slide
							>
								{faq.answer}
							</p>
						{/if}
					</div>
				</Saos>
			{/each}
		</div>
	</div>
</section>

<style lang="scss">
	.faq {
		@include container;

		&__container {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			padding: 64px 32px;

			&__header {
				color: white;
				display: flex;
				flex-direction: column;
				align-items: center;
				margin-bottom: 32px;

				&__subtitle {
					color: $primary-clr;
				}
			}

			&__questions {
				display: flex;
				flex-direction: column;
				width: 100%;
				gap: 16px;

				&__details {
					background-color: #343637;
					padding: 18px 32px;
					color: white;

					&__header {
						display: flex;
						flex-direction: row;
						justify-content: space-between;
						align-items: center;
						cursor: pointer;
						gap: 12px;
					}

					&__text {
						overflow: hidden;
						padding: 22px 0;
						transition: 0.3s ease-in-out;
					}
				}
			}
		}
	}
</style>
