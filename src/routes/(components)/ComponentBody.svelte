<script lang="ts">
	import ComponentChild from './ComponentChild.svelte';
	import { onMount } from 'svelte';
	export let randomConditionalBool: boolean = false;
	export let myObjectItem: { status: string };

	function howCanIBeExecuted() {
		console.log(
			'HOW AM I EXECUTED? The object is ALWAYS defined, but it is undefined just because i dont have bind: on the main parent.'
		);
		return 'CHECK CONSOLE!';
	}

	let dataInitialized: boolean = false;
	onMount(() => {
		dataInitialized = true;
	});
</script>

{#if dataInitialized}
	<ComponentChild {randomConditionalBool} bind:myObjectItem></ComponentChild>

	{#if myObjectItem?.status}
		Is good!
	{:else}
		{howCanIBeExecuted()}
	{/if}
{/if}
