<script>
	import ProjectCard from "../components/ProjectCard.svelte";
	import Footer from '../components/Footer.svelte'
	
	let projects = [
		{
			title: "JNL Website",
			description:
				"Joyful Noise Learning is my wife's web presence for her YouTube channel. Once a public teacher, she now homeschools and helps others get started in the task of schooling from home. This is a Gatsby site that features a blog that pulls data from Contentful (headless CMS) and rebuilds when content changes. I also designed the logo, and promotional art for her eBooks and printed products.",
			tools: ["Tailwind CSS", "React", "Gatsby", "Netlify", "Contentful"],
			image: "joyfulnoiselearning-card.png",
			url: "https://joyfulnoiselearning.com"
		},
		{
			title: "Listen Up",
			description:
				"This project was born out of the need for a tool to test webhooks in realtime. It is a full-stack app that creates an endpoint for you which you can send POST requests to and see the results in realtime. This is useful for testing webhook sending from another webserver. Note: This is hosted on the free tier of Heroku, so it may take a moment to spin up.",
			tools: ["Tailwind CSS", "Vue", "FeathersJS", "Heroku", "MongoDB"],
			image: "listen-up-card.png",
			url: "https://listen-up-yo.herokuapp.com/",
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
		<h1 class="title">Tinker/side Projects</h1>
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
							github={project.github_url}
							tools={project.tools} />
				</div>
			{/each}
		</div>
	</div>
</div>

	<Footer />
