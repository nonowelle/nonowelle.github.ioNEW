<template>
	<section id="projets">
		<div class="wrapper projets">
			<h2
				class=""
				data-sal="slide-up"
				data-sal-delay="200"
				data-sal-duration="800"
			>
				My Projects
			</h2>
			<div
				class="glide"
				ref="glide"
			>
				<div
					class="glide__track"
					data-glide-el="track"
					data-sal="slide-up"
					data-sal-delay="200"
					data-sal-duration="800"
				>
					<ul class="glide__slides">
						<li
							class="glide__slide project-details"
							v-for="project in projects"
							:key="project.id"
						>
							<div class="project-image">
								<img
									:src="project.img"
									alt=""
								/>
							</div>
							<div class="project-text">
								<p class="project-description">
									{{ project.description }}
								</p>
								<div class="title-tech">
									<p>Technologies:</p>
									<div class="tech">
										<li
											v-for="tech in project.techs"
											:key="tech.id"
											class="techs"
										>
											{{ tech.name }}
										</li>
										<div class="btn">
											<a
												target="_blank"
												:href="project.links[0]"
												class="site"
												>Site Web
												<i
													class="fas fa-long-arrow-alt-right lien"
												></i
											></a>
										</div>
										<div
											v-if="project.links[1]"
											class="btn"
										>
											<a
												target="_blank"
												:href="project.links[1]"
												class="site"
												>Code
												<i
													class="fas fa-long-arrow-alt-right lien"
												></i
											></a>
										</div>
									</div>
								</div>
							</div>
						</li>
					</ul>
					<div
						class="glide__arrows"
						data-glide-el="controls"
					>
						<button
							class="glide__arrow glide__arrow--left"
							data-glide-dir="<"
						>
							<i
								class="fas fa-arrow-left"
								ref="fleche"
							></i>
						</button>
						<button
							class="glide__arrow glide__arrow--right"
							data-glide-dir=">"
						>
							<i
								class="fas fa-arrow-right"
								ref="fleche"
							></i>
						</button>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
	import Glide from '@glidejs/glide';

	export default {
		name: 'Projects',
		data: function () {
			return {
				projects: [
					{
						id: 1,
						title: 'Coveo',
						description:
							"I've been part of the Web team at Coveo for almost three years now. I work on a daily basis with Vue js and Sitecore to create responsive and beautiful components. I also make sure Coveo's corporate website is performant and up to the highest standards.",
						img: 'imgs/coveo.png',
						techs: [
							{ name: 'Sitecore', id: 1 },
							{ name: 'Vue.js', id: 2 },
							{ name: 'Sass', id: 3 },
							{ name: 'Cypress', id: 4 },
							{ name: 'Figma', id: 5 },
						],
						links: ['https://www.coveo.com/'],
					},
					{
						id: 2,
						title: 'Planties',
						description:
							"Planties is a complete web app. After signing up, you can collect and share pictures of all your plants with the planties community. You can even comment on your friend's plant and keep track of their growth.",
						img: 'imgs/planties-2.1.png',
						techs: [
							{ name: 'Bootstrap', id: 1 },
							{ id: 2, name: 'Express' },
							{ id: 3, name: 'Node.js' },
							{ id: 4, name: 'MongoDB' },
							{ id: 5, name: 'EJS' },
						],
						links: [
							'https://planties.onrender.com/',
							'https://github.com/nonowelle/planties',
						],
					},

					{
						id: 4,
						title: 'Wedding Site',
						description:
							'I built this webpage to make an online RSVP system for my friends wedding. Every guest answer was saved in a restdb database.',
						img: '/imgs/charlie-benoit-2.png',
						techs: [
							{ name: 'HTML', id: 1 },
							{ name: 'CSS', id: 2 },
							{ name: 'Vue Js', id: 3 },
							{ name: 'Node', id: 4 },
							{ name: 'restDb', id: 5 },
						],
						links: [
							'https://charlie-benoit-wedding-fe.onrender.com/',
							'https://github.com/nonowelle/charlie-benoit',
						],
					},
				],
			};
		},
		methods: {},
		mounted() {
			new Glide(this.$refs.glide, {
				type: 'carousel',
				startAt: 1,
				focusAt: 'center',

				perView: 2.5,
				bound: true,
				gap: 50,
				breakpoints: {
					1024: {
						perView: 1.2,
					},
				},
			}).mount();
		},
	};
</script>
