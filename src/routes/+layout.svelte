<svelte:head>
	<style>
		:root {
			--background-base: white;
			--background-primary: #2f2442;
			--background-secondary: #d6b8ff;
			--text-base: black;
			--text-primary: white;
		}

		@media (prefers-color-scheme: dark) {
			:root {
				--background-base: #181720;
				--background-primary: #d6b8ff;
				--background-secondary: #2f2442;
				--text-base: white;
				--text-primary: black;
			}
		}

		body {
			background-color: var(--background-base);
			color: var(--text-base);

			display: flex;
			flex-direction: column;

			font-family: Arial, 'sans serif';
			font-size: 1.2em;
		}

		.emoji {
			height: 1.2em;
			vertical-align: bottom;
		}
	</style>
</svelte:head>

<slot />
