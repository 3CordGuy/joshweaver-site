<script>
	import Social from '../components/Social.svelte'
	export let segment

	let isActive = false

	function toggleMenu(event) {
		isActive = !isActive
	}

</script>

<style>
	
</style>


<nav class="navbar is-dark" role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
		<a class="navbar-item" href="." aria-current='{segment === undefined ? "page" : undefined}'>
			<strong>joshweaver.dev</strong>
		</a>

		<div role="button" class="navbar-burger burger {isActive && 'is-active'}" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample" on:click={toggleMenu}>
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
		</div>
	</div>

	<div id="navbarBasicExample" class="navbar-menu {isActive && 'is-active'}">
		<div class="navbar-start">
			<a class="navbar-item" href="about" aria-current='{segment === "about" ? "page" : undefined}'>About</a>
			<a class="navbar-item" href="projects" aria-current='{segment === "projects" ? "page" : undefined}'>Projects</a>
		</div>

		<div class="navbar-end">
			<div class="navbar-item">
				<Social color="light" />
			</div>
		</div>
	</div>
</nav>
