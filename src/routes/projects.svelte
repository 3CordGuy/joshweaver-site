<script>
	import ProjectCard from "../components/ProjectCard.svelte";
	import Footer from '../components/Footer.svelte'

	let projects = [
		{
			title: "Coder's Liturgy",
			description:
				"This is a personal passion project to create a resource for myself and other coders of the Christian faith. It is collection of prayers presented cleanly that can help point a heart in the right direction for work. The prayers and their associated icons are all original efforts along with the site layout & design.",
			tools: ["Tailwind CSS", "Sveltekit", "Cloudflare Pages", "ESV API"],
			image: "coders-liturgy-card.png",
			url: "https://codersliturgy.com",
			github_url: "https://github.com/3Cordguy/coders-liturgy"
		},
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
				"This project was born out of the need for a tool to test webhooks in realtime. It is a full-stack app that creates an endpoint for you which you can send POST requests to and see the results in realtime. This is useful for testing webhook sending from another webserver.",
			tools: ["Tailwind CSS", "Vue", "FeathersJS", "Fly.io", "MongoDB"],
			image: "listen-up-card.png",
			url: "https://heylistenup.app/",
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
		},
		{
			title: "Alphabet Emojifier",
			description:
				"Convert text to Slack's alphabet emojis. This is a little demo project that uses Cloudlfare workers to run a string processing script that turns your text into slack alphabet emojis. Server rendered results run entirely on the Cloudflare edge.",
			tools: ["Cloudflare Workers", "Raw HTML/css", "Vanilla JS"],
			image: "alphabet-emojifier-card.png",
			url: "https://alphabet-emojifier.3cordguy.workers.dev/",
			github_url: "https://github.com/3CordGuy/alphabet-emojifier"
		}
	];
</script>

<style>
.project-cards {
	margin-top: 2rem;
	display: grid;
	gap: 2rem;
	grid-template-columns: repeat(2, 50%);
}

@media (max-width: 767.98px) {
	.project-cards {
		grid-template-columns: 100%;
	}
}
</style>

<svelte:head>
	<title>Josh Weaver : Projects</title>
</svelte:head>

<div class="section">
	<div class="container">
		<h1 class="title">Hobby Projects</h1>
	</div>
	<div class="container">
		<div class="project-cards">
			{#each projects as project}
			<ProjectCard
			title={project.title}
			image={project.image}
			description={project.description}
			url={project.url}
			github={project.github_url}
			tools={project.tools} />
				{/each}
		</div>
	</div>
</div>

	<Footer />
