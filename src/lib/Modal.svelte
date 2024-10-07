<script>

    export let showModal;
    let dialog;

    $: if(dialog && showModal) dialog.showModal();

</script>

<!-- svelte-ignore a11y-click-events-have-key-events a11y-no-noninteractive-element-interactions -->
<dialog
	bind:this={dialog}
	on:close={() => (showModal = false)}
	on:click|self={() => dialog.close()}
>
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<div on:click|stopPropagation>
        <section class="controls-section">
            <!-- svelte-ignore a11y-autofocus -->
            <button autofocus on:click={() => dialog.close()}></button>
            <button></button>
            <button></button>
        </section>
		<slot name="video-1">
        </slot>
        <slot name="video-2" />
        <slot name="video-3" />
	</div>
</dialog>

<style>
	dialog {
        background-color: #171919;
		max-width: 85%;
		border-radius: .5em;
		border: none;
		padding: 0;
	}
	dialog::backdrop {
		background: rgba(0, 0, 0, 0.3);
	}
	dialog > div {
		padding: 1.5em;
	}
	dialog[open] {
		animation: zoom 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
	}
	@keyframes zoom {
		from {
			transform: scale(0.95);
		}
		to {
			transform: scale(1);
		}
	}
	dialog[open]::backdrop {
		animation: fade 0.2s ease-out;
	}
	@keyframes fade {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

    .controls-section {
        display: flex;
        gap: .7em;
        margin-bottom: 1em;
    }

    button {
        padding: 1em;
        border: none;
        background-color: rgb(252, 23, 23);
        border-radius: 50%;
    }

    button:nth-child(2){
        background-color: gray;
    }

    button:nth-child(3){
        background-color: rgb(34, 223, 34);
    }
</style>

