<script>
export let title
export let subtitle
export let url
export let tools
export let description
export let image
export let github
</script>

<style>
	.card-content {
		min-height: 300px;
	}
	.card {
		border-radius: 1rem;
		overflow:hidden;
	}
</style>
<div class="card">
	<div class="card-image">
		<figure class="image">
			<img src="{image}" alt="{title} Project by Josh Weaver">
		</figure>
	</div>
	<div class="card-content">
		<div class="media">
			<div class="media-content">
				<p class="title is-4">{title}</p>
				{#if subtitle}<p class="subtitle is-6">{subtitle}</p>{/if}
			</div>
		</div>

		<div class="content">
			<p>{description}</p>
			<div class="tags">
				{#each tools as tool}
					<span class="tag">
						{tool}
					</span>
				{/each}
			</div>

		</div>
	</div>
	<footer class="card-footer">
		<a href="{url}" class="card-footer-item">View {title}</a>
		{#if github}<a href="{github}" class="card-footer-item"><span class="icon is-small"><i class="fab fa-1x fa-github"></i></span>&nbsp;Source</a>{/if}
	</footer>
</div>
