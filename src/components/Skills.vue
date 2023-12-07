<template>
	<section
		class="skills"
		id="skills"
	>
		<div class="wrapper">
			<h2 class="comp">{{ title.en }}</h2>

			<div class="">
				<ul class="grid">
					<li
						v-for="link in links"
						:key="link.src"
						class="logo"
					>
						<img
							:src="link.src"
							alt=""
						/>
					</li>
				</ul>
			</div>
		</div>
	</section>
</template>

<script>
	export default {
		name: 'Skills',
		data() {
			return {
				title: {
					fr: 'Compétences',
					en: 'Skills',
				},
				links: [
					{
						src: 'imgs/html5-css3-js.png',
					},
					{
						src: 'imgs/sass.png',
					},
					{
						src: 'imgs/vue.png',
					},
					{
						src: 'imgs/jquery.png',
					},
					{
						src: 'imgs/node-js.png',
					},
					{
						src: 'imgs/figma-1-logo-png-transparent.png',
					},
					{
						src: 'imgs/tag-manager.png',
					},
					{
						src: 'imgs/sitecore.png',
					},
					{
						src: 'imgs/cypress.svg',
					},
					{
						src: 'imgs/gulp.svg',
					},
				],
			};
		},
	};
</script>
