<script>
	export let message = 'default value';
	export let showModal = false;
</script>

{#if showModal}
	<div class="modal">
		<div class="modal-body">
			<button class="modal-btn-close" on:click>x</button>
			<div class="modal-inner">
				<p>Hi!</p>
				<p>{message}</p>
			</div>

			<button class="modal-btn-submit" on:click>확인</button>
		</div>
	</div>
{/if}

<style>
	.modal {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		padding: 3vh;
		width: 80%;
		background: rgb(255, 255, 255, 0.8);
		border-radius: 15px;
		border: 2px solid rgba(256, 256, 256, 0.7);
		font-size: 3vh;
		color: #000;
		text-align: center;
	}

	.modal-inner {
		margin: 3%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		line-height: 1.3;
		flex-direction: column;
	}

	.modal-btn-close {
		position: absolute;
		top: 15px;
		right: 15px;
		border: none;
		background: none;
		cursor: pointer;
		font-size: 1.7rem;
	}

	.modal-btn-submit {
		margin: 0.5rem 0;
		color: white;
		padding: 0.3rem;
		background-color: var(--color-theme-2);
		cursor: pointer;
	}
</style>
