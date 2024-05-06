<script lang="ts">
	export let pageLoading: boolean = false;
</script>

{#if pageLoading}
	<p>Page loading...</p>
{:else}
	<slot name="page-heading" />

	<slot name="body-header" />

	<slot name="body" />
{/if}

<style>
</style>
