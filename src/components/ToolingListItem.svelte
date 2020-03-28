<script>
export let isHeading
export let text
export let icon
</script>

<style>
	.list-item-child {
		padding-left: 1rem;
	}
</style>

<li class="list-item">
	{#if isHeading}
		<h4 class="subtitle is-5 has-text-dark">
			{text}
		</h4>
	{:else}
		<span class="list-item-child">{text}</span>
		{#if icon}<span class="icon"><i class="fab fa-{icon}"></i></span>{/if}
	{/if}
</li>