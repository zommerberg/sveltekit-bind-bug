<script lang="ts">
	import { onMount, tick } from 'svelte';
	import ComponentBody from './(components)/ComponentBody.svelte';
	import ComponentHeader from './(components)/ComponentHeader.svelte';
	import LayoutManager from './(components)/LayoutManager.svelte';

	let pageLoading: boolean = false;
	let myObjectItem: { status: string } = { status: 'Good' };

	let randomConditionalBool: boolean = false;
</script>

<LayoutManager {pageLoading}>
	<svelte:fragment slot="page-heading">
		<ComponentHeader bind:randomConditionalBool></ComponentHeader>
	</svelte:fragment>

	<svelte:fragment slot="body">
		<ComponentBody {myObjectItem} {randomConditionalBool}></ComponentBody>
	</svelte:fragment>
</LayoutManager>
