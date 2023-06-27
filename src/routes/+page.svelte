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

<div class="infoblock">
	<p>
		Haii, welcome to our silly little page. Might as well introduce ourselves, it's the least we can
		do :catresort:
	</p>

	<p>
		We're a system of <a href="https://fronters.ringlings.systems/all">{memberCount}</a> known collectively
		as Gem. We do random stuff sometimes. All times, actually. What kinda stuff? Welllllll...
	</p>
</div>

<div class="right-anchor infoblock">
	<p>
		We do programming I guess! It's one of our special interests so when we can actually meet the
		other requirements (spoons, ideas, whatnot)<br /> it's a really fun thing to do. Except when nothing
		works, that always sucks.
	</p>
	<p>
		You can find our portfolio of random stuff at our <a href="https://github.com/Ringlings">GitHub</a>.
	</p>
</div>

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

	.infoblock {
		max-width: 75%;
		background-color: var(--background-secondary);
		padding: 5px;
		border-radius: 10px;
		margin-top: 20px;
		margin-left: 5%;
		margin-right: 5%;
	}

	.infoblock p {
		margin-top: 10px;
		margin-bottom: 10px;
		margin-left: 10px;
		margin-right: 10px;
	}

	.right-anchor {
		align-self: flex-end;
		align-items: flex-end;
		text-align: end;
	}

	a {
		color: mediumslateblue;
	}
</style>
