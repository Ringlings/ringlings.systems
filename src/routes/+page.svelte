<script>
	let memberCount = 'at least 2';

	async function load() {
		const response = await fetch('https://api.pluralkit.me/v2/systems/vgspl/members');
		const result = await response.json();

		memberCount = result.length
	}

	load()
</script>

<svelte:head>
	<title>Ringlings System</title>
</svelte:head>

<div class="namedrop">
	<h1>Ringlings</h1>
	<p>Chaotic collective.</p>
</div>

<p>
	Haii, welcome to our silly little page. Might as well introduce ourselves, it's the least we can
	do :catresort:
</p>

<p>
	We're a system of <span
		title="yes This Number Doesn't Load Immediately. no We're Not Gonna Fix It"
	>
		{memberCount}
	</span> known collectively as Gem. We do random stuff sometimes. All times, actually.
</p>

<style>
	.namedrop {
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.namedrop h1 {
		margin-bottom: 0em;
	}
	.namedrop p {
		margin-top: 0em;
	}
</style>
