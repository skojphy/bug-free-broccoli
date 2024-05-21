<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import cat from '$lib/images/characters/cat.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>냥냥보를 찾아서</h1>

	<a class="start" href="./game">START</a>

	<a class="how-to-play" href="./how-to-play">How to play</a>

	<img class="nyang" src={cat} alt="냥냥이" />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		font-size: 2rem;
		width: 100%;
	}

	.start {
		margin: 2rem;
		padding: 1rem;
		font-size: 1.5rem;
		background-color: var(--color-theme-2);
		color: var(--color-text);
	}

	.how-to-play {
		color: var(--color-text);
	}

	.how-to-play::before {
		content: 'i';
		display: inline-block;
		font-size: 0.8em;
		font-weight: 900;
		width: 1em;
		height: 1em;
		padding: 0.2em;
		line-height: 1;
		border: 1.5px solid var(--color-text);
		border-radius: 50%;
		text-align: center;
		margin: 0 0.5em 0 0;
		position: relative;
		top: -0.05em;
	}

	.nyang {
		width: 30%;
		margin: 1rem;
	}
</style>
