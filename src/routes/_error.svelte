<script>
  	import { onMount } from 'svelte';
	export let status;
	export let error;

	const dev = process.env.NODE_ENV === 'development';

	onMount(() => { 
		// auto redirect to home after 5 seconds
		setTimeout(function() {  window.location=window.location.origin; }, 3000);  
	});
</script>

<svelte:head>
	<title>Error {status}</title>
</svelte:head>

<div class="py-5 lg:py-12 text-center">
	<h1 class="font-bold text-2xl">{status}</h1>

	<p class="text-lg">{error.message}</p>

	{#if dev && error.stack}
		<pre>{error.stack}</pre>
	{/if}

</div>