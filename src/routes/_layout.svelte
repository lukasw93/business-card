<script>
	import Nav from '../components/Nav.svelte';
	import PersonConfig, { person } from '../components/PersonConfig.svelte';
	export let segment;
</script>

<svelte:head>
	<meta name="description" content="Business card website of {person.fullname}">
</svelte:head>

<style>
</style>

<div class="z-40 rounded-lg border border-gray-300 flex flex-wrap bg-gray-100 z-50 m-4 sm:m-8 md:m-12 shadow-xl">
	<div class="relative z-10 overflow-hidden w-full lg:w-1/2">
		<img class="z-10 rounded-lg object-cover overflow-hidden lg:min-h-64" src="{person.imageFileName}" alt="{person.fullname}" />
		<svg class="z-0 -mr-48 overflow-hidden hidden absolute top-0 right-0 inset-y-0 lg:inline text-gray-100 w-100 h-full fill-current" preserveAspectRatio="none" viewBox="0 0 100 100">
			<polygon points="60,0 20,0 40,100 80,100"/>
		</svg>
		<svg class="z-10 inline overflow-y-hidden lg:hidden absolute inset-x-0 w-full fill-current text-gray-100 h-64 -mt-16  overflow-hidden" preserveAspectRatio="none" viewBox="0 0 100 100">
			<polygon class="z-10 overflow-hidden" points="0,10 100,20 100,40 0,30"/>
		</svg>
	</div>
	<div class="z-10 relative min-h-full w-full lg:w-1/2 h-full fill-current">
		<Nav {segment}/>
		
		<main class="z-40 relative mx-auto h-full min-h-full fill-current pb-6 lg:pb-0">
			<slot></slot>
		</main>
	</div>
</div>
<div class="-m-2 sm:-m-6 md:-mt-10 text-center font-thin antialiased text-gray-500 mx-auto text-xs">&copy;&nbsp;{person.fullname}&nbsp;{(new Date().getFullYear())}. <span>Icons from <a target="_blank" href="https://icons8.com/">Icons8.com</a></span></div>