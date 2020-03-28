<script>
import ToolingListItem from '../components/ToolingListItem.svelte'
import Footer from '../components/Footer.svelte'

let languages = [{ text: 'JavaScript (es6+)', icon: 'js-square' }, { text: 'Lua' }]
let FrontEnd = [{ text: 'React', icon: 'react' }, { text: 'Vue', icon: 'vuejs' }, { text: 'Svelte' }]
let BackEndFull = [{ text: 'Meteor' }, { text: 'Sapper' }, { text: 'Koa' }, { text: 'Feathers' }]
let StaticSiteGen = [{ text: 'Gatsby' }, { text: 'Eleventy' }]
let DataLayer = [{ text: 'MongoDB' }, { text: 'MySQL' }]
let GraphicsDesign = [{ text: 'Adobe Products (Ps, Ai, iD)', icon: 'adobe' }, { text: 'Affinity Software by Serif (Designer, Photo)' }]
let Cloud = [{ text: 'Zeit Now' }, { text: 'Netlify' }, { text: 'Digital Ocean', icon: 'digital-ocean' }, { text: 'AWS Lambda', icon: 'aws' }]

</script>

<style>
.main-background {
	background: url(josh-smiles-too.jpg) no-repeat center center fixed; 
	-webkit-background-size: cover;
	-moz-background-size: cover;
	-o-background-size: cover;
	background-size: cover;
}

.box {
	background: rgba(255,255,255,0.9);
}
</style>

<svelte:head>
	<title>about</title>
</svelte:head>

<div class="section main-background">
	<div class="container">
		<div class="columns">
			<div class="column is-half-tablet">
				<div class="box">
					<h1 class="title">A little about me...</h1>
					<h3 class="subtitle">Coding <em>is</em> a creative process.</h3>
					<p>I've been coding since 2010 and developing web apps since 2012, but first things first.</p>
					<p>I'm a geek. I love technology and software. I love board games like Scythe and Wingspan. I love Lord of the Rings and Star Wars (the original trilogy) and I don't quite understand why Tom Bombadil didn't make the cut for Peter Jackson. But I guess that's not important.</p>
					<p>When I'm not coding or staring at my computer trying to solve problems, I am usually found playing guitar, ukulele or testing out a new song. I consider myself a singer-songwriter who plays semi-regularly at coffee shops and the occasional open mic night.</p>
					<p>&nbsp;</p>
					<p>So how did I get into coding (when I never thought I would like it)?</p>
					<p>&nbsp;</p>
					<p>I grew up in the Midwest and studied a bit of music, art, and design in college. I moved out west to chase some dreams in 2005. I didn't expect that I would be soaking in the colors and designs of thousands of full-color print jobs at one of the west's largest printing companies in the region. One thing led to another and within a few years, I found myself working freelance graphic design for clients across the United States.</p>
					<p>&nbsp;</p>
					<p>I've had the priviledge of working with Corona Labs (back when they were still called Ansca Mobile) a premier mobile app SDK platform based out of Silicon Valley. During this time, I used my experience with this mobile app SDK to work on some new skills. I launched a couple children's apps into the App Store and a mobile app for a handwriting specialist on the east coast. After all, In 2010, mobile app development was still a new and prime opportunity.</p>
					<p>&nbsp;</p>
					<p>Around 2012, my wife and I ended up moving back to the Midwest for a job. I landed at a software shop that made products for Non-profit and Church Management. The next several years at this company proved to be pretty amazing. Not only did I get to use my graphic design skills, but also documentation, content-writing, marketing videos were all things I added to my toolbelt of experience. But the icing on the cake was that I grew enough to develop web applications from the ground up. Tools that people could use. Tools that <em>WE</em> used.</p>
					<p>&nbsp;</p>
					<p>These were projects that I was proud to call my own because I scoured the internet for best practices, pored over documentation, and spent hours of work building. Projects like:</p>
					<ul>
						<li>- Web app add-on products to compliment the desktop software that allowed users to check-in for group/class attendance.</li>
						<li>- An in-house CRM platform that included Contact management, invoicing, bug tracking, emailing, and payment handling.</li>
						<li>- A completely new event registration SaaS platform that could sell tickets and merchandice with a monthly subscription fee.</li>
					</ul>
					<p>&nbsp;</p>
					<p>And since then I've been performing the role of JavaScript developer for a fully-distributed team that builds fundraising and event registration software.</p>
					<p>&nbsp;</p>
					<p>Though my journey started with graphic design for print and web, I've ended up slinging script in a code editor. I wouldn't have expected this transition, but this work has solidified a realization in my mind. Coding is a creative process. From ideation, to iteration, to realization. Though the landscape is ever changing and new practices and frameworks pop up each day, I love being a part of this community of JavaScript developers.</p>
					<p>&nbsp;</p>
					<p>I can't wait to see where this wind blows next.</p>
				</div>
			</div>
			<div class="column is-4 is-half-tablet">
				<div class="box">
					<h2 class="title has-text-dark">Tooling</h2>
					<h3 class="subtitle">My Mac is my workbech. These are my tools.</h3>
					<ul class="">
						<ToolingListItem isHeading={true} text="Programming" icon='' />
						{#each languages as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}
						
						<ToolingListItem isHeading={true} text="Frontend Frameworks" icon='' />
						{#each FrontEnd as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}

						<ToolingListItem isHeading={true} text="Backend/Full-stack Frameworks" icon='' />
						{#each BackEndFull as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}

						<ToolingListItem isHeading={true} text="Static Site Generators" icon='' />
						{#each StaticSiteGen as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}

						<ToolingListItem isHeading={true} text="Data Layer" icon='' />
						{#each DataLayer as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}

						<ToolingListItem isHeading={true} text="Graphics & Design" icon='' />
						{#each GraphicsDesign as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}

						<ToolingListItem isHeading={true} text="Serverless & Hosting" icon='' />
						{#each Cloud as item}
							<ToolingListItem isHeading={false} text={item.text} icon={item.icon} />
						{/each}
					</ul>
				</div>
			</div>
		</div>
	</div>
</div>
<Footer>
	<p>Photo Credit: <a href="https://www.instagram.com/greyz.dev/">Greyson Zittle</a></p>
</Footer>
