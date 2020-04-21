<script>
	export let segment;
</script>

<nav class="z-10 -mt-6 md:mt-0 mx-auto text-base md:text-lg">
	<ul class="mx-auto">
		<li><a aria-current='{segment === undefined ? "page" : undefined}' href='.'>card</a></li>
		<li><a aria-current='{segment === "person" ? "page" : undefined}' href='person'>person</a></li>
		<li><a aria-current='{segment === "big-five" ? "page" : undefined}' href='big-five'>big five</a></li>
		<li><a aria-current='{segment === "code" ? "page" : undefined}' href='code'>code</a></li>
	</ul>
</nav>