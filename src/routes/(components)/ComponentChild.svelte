<script lang="ts">
	import ComponentChildChild from './ComponentChildChild.svelte';

	export let myObjectItem: { status: string };
	export let randomConditionalBool: boolean;
</script>

{#if !randomConditionalBool}
	<ComponentChildChild bind:myObjectItem></ComponentChildChild>
{/if}
