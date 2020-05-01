<svelte:head>
	<title>Enter Code - Lukas Weichselbraun</title>
</svelte:head>

<div class="py-12 lg:py-16 xl:py-32">
  <form class="mx-auto max-w-xs pl-5" onSubmit="return false;">
      <label class="block text-gray-700 text-sm font-bold mb-1" for="code">
        Code
      </label>
    <div class="inline-flex items-center justify-center">
      <input bind:value={code} class="shadow appearance-none border rounded w-auto py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
      id="code" type="text" placeholder="Enter your code" />
    
      <button id="btnGo" type="button" on:click={openCode} class="ml-2 bg-blue-500 hover:bg-blue-700 w-auto text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline">
        Go
      </button>
    </div>
  </form>
</div>

<!-- needed for sapper export build -->
<!-- remove this div in exported file to keep links secret -->
<div class="hidden">
		<a href='code/007'>hidden link</a>
</div>

<script>
  let code;
  
	function openCode() {
		location.href = window.location.origin + "/code/" + code;
  }
</script>