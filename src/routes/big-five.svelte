<script>
  import PersonConfig, { person } from '../components/PersonConfig.svelte';
</script>

<svelte:head>
	<title>Big Five - {person.fullname}</title>
</svelte:head>



<div class="pt-4 xl:pt-12 z-40 grid grid-cols-1 text-center gap-5 text-base md:text-lg text-gray-800">
	{#each person.bigFiveHtmlItems as bigFive}
		<div>{@html bigFive}</div>
	{/each}
</div>