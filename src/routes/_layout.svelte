<script>
	import Nav from '../components/Nav.svelte';
	import SideBar from '../components/SideBar.svelte'


	export let segment
	let isSidebar = false

	const handleSidebar = () => {
		isSidebar = !isSidebar
	}

</script>

<style>
</style>

<div class="off-canvas">
  <div id="sidebar" class="off-canvas-sidebar { isSidebar === true ? 'active' : ''}">
    <SideBar></SideBar>
  </div>

  <div class="off-canvas-overlay"  on:click|preventDefault={handleSidebar} ></div>

  <div class="off-canvas-content">
		<Nav {segment} on:click={handleSidebar} {isSidebar}  />
		<main>
		    <slot></slot> 
		</main>
  </div>
</div>