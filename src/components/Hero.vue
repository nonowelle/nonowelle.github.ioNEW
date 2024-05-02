<template>
	<div
		class="hero"
		id="#hero"
		ref="hero"
	>
		<Header />
		<div class="wrapper">
			<section class="accueil">
				<div class="triangles">
					<div class="un"></div>
					<div class="deux"></div>
					<div class="trois"></div>
					<div class="quatre"></div>
					<div class="cinq"></div>
				</div>
				<div class="texte">
					<h1>
						Hello! <br />
						I'm <span class="nom">Marie-Ève</span>.
					</h1>
					<p class="description">
						I'm a French Canadian Frontend developer based in
						Madrid. I'm passionate about pixel-perfect beautiful
						interfaces and I love to add a magic touch to the
						internet.
					</p>
				</div>
			</section>
		</div>
	</div>
</template>

<script>
	import Header from './Header.vue';
	export default {
		name: 'Hero',
		components: {
			Header,
		},
		data: function () {
			return {
				isUserScrolling: false,
			};
		},
	};
</script>
