<script>
	import ProjectCard from "../components/ProjectCard.svelte";
	import Footer from '../components/Footer.svelte'
	
	let projects = [
		{
			title: "Listen Up",
			description:
				"This project was born out of the need for a tool to test webhooks in realtime. It is a full-stack app that creates an endpoint for you which you can send POST requests to and see the results in realtime. This is useful for testing webhook sending from another webserver. Note: This is hosted on the free tier of Zeit Now, so it may take a moment to spin up.",
			tools: ["Tailwind CSS", "Vue", "FeathersJS", "Zeit Now", "MongoDB"],
			image: "listen-up-card.png",
			url: "https://listenup.now.sh",
			github_url: "https://github.com/3Cordguy/listen-up"
		},
		{
			title: "Happy Trees",
			description:
				"I know you can generate ascii file trees from the command line. But wouldn't it be fun if you could generate them from a few lines of Markdown? Yeah, I thought so, too—which is why I built this. I use it when I am writing documentation. This is a simple frontend web app hosted on Netlify. It uses Bulma for CSS and some helpful Markdown parsing libraries.",
			tools: ["Bulma", "Vue", "Netlify"],
			image: "happy-trees-card.png",
			url: "https://happytrees.netlify.app",
			github_url: "https://github.com/3CordGuy/happy-trees"
		}
	];
</script>

<style>
.project-cards {
	margin-top: 2rem;
}
</style>

<svelte:head>
	<title>Josh Weaver : Projects</title>
</svelte:head>

<div class="section">
	<div class="container">
		<h1 class="title">Tinker Projects</h1>
	</div>
	<div class="container project-cards">
		<div class="columns">
			{#each projects as project}
				<div class="column is-4">
						<ProjectCard
							title={project.title}
							image={project.image}
							description={project.description}
							url={project.url}
							tools={project.tools} />
				</div>
			{/each}
		</div>
	</div>
	<Footer />
</div>

