<script>
	import { onMount } from 'svelte';

	let memberCount = '...';

	onMount(async () => {
		const response = await fetch('https://api.pluralkit.me/v2/systems/vgspl/members');
		const result = await response.json();

		memberCount = result.length;
	});
</script>

<svelte:head>
	<title>Ringlings System</title>
</svelte:head>

<div class="namedrop">
	<h1>Ringlings</h1>
	<p>Chaotic collective</p>
</div>

<p>
	Haii, welcome to our silly little page. Might as well introduce ourselves, it's the least we can
	do :catresort:
</p>

<p class="left-anchor">
	We're a system of <a href="https://fronters.ringlings.systems/all">{memberCount}</a> known collectively
	as Gem. We do random stuff sometimes. All times, actually. What kinda stuff? Welllllll...
</p>

<style>
	.namedrop {
		padding: 10px;
		border-radius: 10px;

		display: flex;
		flex-direction: column;
		align-items: center;
		align-self: center;

		background-color: var(--background-primary);
		color: var(--text-primary);
	}
	.namedrop * {
		margin: 0em;
		max-width: fit-content;
		background-color: unset;
	}

	p {
		max-width: 75%;
		background-color: var(--background-secondary);
		padding: 5px;
		border-radius: 10px;
		margin-left: 5%;
		margin-right: 5%;
	}

	.left-anchor {
		align-self: flex-end;
		text-align: end;
	}

	a {
		color: mediumslateblue;
	}
</style>
