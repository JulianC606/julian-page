<script>
	export let segment;
	export let isSidebar = false
</script>

<style>
	header {
		background-color: #fafafa
	}
	#cover{
		height: 2em;
	}
</style>

<header class="navbar p-2">
  <section class="navbar-section">
    <a href='.' aria-current='{segment === undefined ? "page" : undefined}' class="navbar-brand mr-2">
			<img src="logo.svg" alt="JulianC" id='cover'>
		</a>
  </section>
  <section class="navbar-section pr-2">
		
		<a href='javascript.void(0)' on:click|preventDefault>
			<i class="icon {isSidebar ? 'icon-cross' : 'icon-menu'} icon-2x"></i>
		</a>
  </section>
</header>
