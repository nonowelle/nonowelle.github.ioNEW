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
								<div class="title-tech">
									<p>Technologies:</p>
									<ul class="tech">
										<li
											v-for="tech in project.techs"
											:key="tech.id"
											class="techs"
										>
											{{ tech.name }}
										</li>
									</ul>
									<div class="btn">
										<a
											target="_blank"
											:href="project.links[0]"
											class="site"
											>Site Web
											<svg
												xmlns="http://www.w3.org/2000/svg"
												viewBox="0 0 448 512"
											>
												<!--!Font Awesome Free 6.5.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
												<path
													d="M438.6 278.6c12.5-12.5 12.5-32.8 0-45.3l-160-160c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L338.8 224 32 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l306.7 0L233.4 393.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l160-160z"
												/></svg
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
											<svg
												xmlns="http://www.w3.org/2000/svg"
												viewBox="0 0 448 512"
											>
												<!--!Font Awesome Free 6.5.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
												<path
													d="M438.6 278.6c12.5-12.5 12.5-32.8 0-45.3l-160-160c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L338.8 224 32 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l306.7 0L233.4 393.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l160-160z"
												/>
											</svg>
										</a>
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
							<svg
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 320 512"
							>
								<!--!Font Awesome Free 6.5.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
								<path
									d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"
								/>
							</svg>
						</button>
						<button
							class="glide__arrow glide__arrow--right"
							data-glide-dir=">"
						>
							<svg
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 320 512"
							>
								<!--!Font Awesome Free 6.5.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
								<path
									d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"
								/>
							</svg>
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

				perView: 3,
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
