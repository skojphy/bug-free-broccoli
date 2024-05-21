<script>
	import cat from '$lib/images/characters/cat2.png';
	import photo1 from '$lib/images/photos/photo1.jpeg';
	import Icon from '@iconify/svelte';
	import Modal from '$components/Modal.svelte';

	let showModal = false;

	const toggleModal = (btnNo) => {
		showModal = !showModal;
		message = `냥 ${btnNo}`;
	};

	let message = '';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="wrap">
	<h1>냥냥보를 찾아서 1</h1>

	<div class="photo-container">
		<img class="photo" src={photo1} alt="사진1" />
	</div>

	<div class="icon-container">
		<Icon icon="mdi:search-add-outline" style="font-size: 36px" />
	</div>

	<div class="dialogue-container">
		<div class="profile-box">
			<img class="profile" src={cat} alt="냥냥이" />
		</div>
		<div class="dialogue-box">
			<p class="text">하이!</p>
			<p class="text">아무거나 골라 봐</p>
			<button class="option" on:click={() => toggleModal(1)}>선택지1</button>
			<button class="option" on:click={() => toggleModal(2)}>선택지2</button>
		</div>
	</div>

	<Modal {message} {showModal} on:click={toggleModal} />
</div>

<style>
	.wrap {
		display: flex;
		flex: 1;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	.icon-container {
		position: fixed;
		top: 50%;
		left: 50%;
	}

	h1 {
		font-size: 1.5rem;
		margin: 2rem auto;
	}

	.photo-container {
		display: flex;
		justify-content: center;
	}

	.photo {
		width: 40%;
	}

	.dialogue-container {
		display: flex;
		width: 90%;
		height: 200px;
		position: absolute;
		left: 5%;
		bottom: 5%;
		padding: 1.5rem;
		box-sizing: border-box;
		background-color: rgb(255, 255, 255, 0.25);
		border-radius: 10px;
	}

	.profile-box {
		width: 15%;
		margin-right: 1.5rem;
	}

	.profile {
		width: 100%;
	}

	.text {
		line-height: 1.7rem;
	}

	.option {
		display: block;
		margin: 0.5rem 0;
		/* color: var(--color-bg-0); */
		color: var(--color-theme-1);
		padding: 0.3rem;
		background-color: var(--color-theme-2);
		cursor: pointer;
	}
</style>
