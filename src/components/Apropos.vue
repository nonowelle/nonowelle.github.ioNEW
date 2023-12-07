<template>
	<div
		class="apropos"
		id="apropos"
	>
		<div class="wrapper">
			<h2 class="titre-apropos">{{ title }}</h2>
			<p class="para">
				{{ texte }}
			</p>

			<div class="parcours">
				<div class="etudes">
					<div class="entries">
						<ul>
							<li
								v-for="entry in entries"
								:key="entry.title"
								class="entry"
								ref="entry"
							>
								<p class="title">{{ entry.title }}</p>
								<div class="desc">
									<ul>
										<li
											v-for="job in entry.jobs"
											:key="job.jobTitle"
										>
											<div class="desc">
												<p class="job-title">
													{{ job.jobTitle }}
												</p>
												<p class="job-desc">
													{{ job.jobDesc }}
												</p>
											</div>
										</li>
									</ul>
								</div>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Apropos',
		data() {
			return {
				title: 'About me',
				texte: "Before getting into web development, I worked in marketing for a few years. I'm passionnate about learning new languages - linguistic or programmatic. I mostly work in Vue.js but I'm always looking to try new technologies.",
				entries: [
					{
						title: 'May 2021 - Today',
						jobs: [
							{
								jobTitle: 'Front-End Developer - Coveo',
								link: 'https://www.coveo.com/',
								jobDesc:
									'SCSS - JS - Vue - GTM - Figma - Cypress - Sitecore - Gulp - Performance - Design',
							},
						],
					},
					{
						title: '2020',
						jobs: [
							{
								jobTitle: 'Webmaster - CRISM',
								link: 'https://www.crismquebecatlantic.ca/',
								jobDesc:
									'Wordpress - Design - SEO - Copy Writing - Content Integration',
							},

							{
								jobTitle: 'The Modern Javascript Bootcamp',
								link: 'https://www.udemy.com/course/javascript-beginners-complete-tutorial/',
								jobDesc: 'Ongoing',
							},
							{
								jobTitle:
									'The Web Developer Bootcamp 2020 Certification',
								link: 'https://www.udemy.com/course/the-web-developer-bootcamp/',
								jobDesc: 'Completed',
							},
						],
					},
					{
						title: '2019',
						jobs: [
							{
								jobTitle: 'Management DESS - ESG',
							},
						],
					},
					{
						title: '2018-2019',
						jobs: [
							{
								jobTitle:
									'Marketing Agent- Druide informatique',
								link: 'www.druide.com',
								jobDesc:
									'SEO - Marketing - Web integration - Partnerships - Copy Writing',
							},
						],
					},
				],
			};
		},
	};
</script>
