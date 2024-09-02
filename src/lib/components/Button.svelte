<script lang="ts">
	export let placeholder;
	export let type: 'fill' | 'border' = 'fill';
</script>

<button class:button--fill={type === 'fill'} class:button--border={type === 'border'}
	>{placeholder}</button
>

<style lang="scss">
	.button {
		&--fill {
			padding: 0.5rem 1rem;
			color: black;
			background-color: white;
			border: none;
			font-size: 1.2rem;
			font-weight: 700;
			border-radius: 8px;
			border: 2px solid white;
			cursor: pointer;
			transition: 0.3s ease-in-out;

			&:hover {
				background-color: $primary-clr;
				border: 2px solid $primary-clr;
			}
		}

		&--border {
			padding: 0.5rem 1rem;
			color: white;
			background-color: transparent;
			border: 2px solid white;
			font-size: 1.2rem;
			font-weight: 700;
			border-radius: 8px;
			cursor: pointer;
			transition: 0.3s ease-in-out;

			&:hover {
				color: $primary-clr;
				border: 2px solid $primary-clr;
			}
		}
	}
</style>
