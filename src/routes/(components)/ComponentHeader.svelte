<script lang="ts">
	import { onMount } from 'svelte';

	export let randomConditionalBool: boolean = false;

	onMount(async () => {
		randomConditionalBool = true;
	});
</script>
