<script>
import Social from '../components/Social.svelte'
</script>


<style>
.main-background {
	background: url(trees.jpg) no-repeat center center fixed; 
	-webkit-background-size: cover;
	-moz-background-size: cover;
	-o-background-size: cover;
	background-size: cover;
}

figure {
	margin-bottom: 1rem;
}
</style>

<svelte:head>
	<title>Josh Weaver</title>
</svelte:head>


<section class="hero is-dark is-fullheight-with-navbar main-background">
	<div class="hero-body">
		<div class="container">
			<div class="columns">
				<div class="column is-three-quarters">
					<figure class="image is-128x128">
						<img alt="Josh Weaver is a JavaScript Developer from the Midwest" class="is-rounded" src="josh-headshot.png">
					</figure>
					<h1 class="title is-1">
						Hello, I'm Josh Weaver
					</h1>
					<h2 class="subtitle">
						I make things with JavaScript
					</h2>
					<Social color="light" />
				</div>
			</div>
		</div>
	</div>
</section>
