<script>
  import PersonConfig, { person } from '../components/PersonConfig.svelte';
</script>

<svelte:head>
	<title>Person - {person.fullname}</title>
</svelte:head>


<div class="grid grid-cols-2 pt-4 pb-2 lg:pb-0 xl:pt-12 gap-2 -ml-4 text-sm sm:text-base xl:text-lg">
  {#each person.aboutHtmlItems as about}
    <div class="text-right text-gray-700 mr-4">{@html about.key}</div>
    <div>{@html about.value}</div>
  {/each}
</div>
