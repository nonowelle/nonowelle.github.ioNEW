<template>
	<div id="app">
		<Header />
		<Hero />
		<Apropos />
		<Skills />
		<Projects />
		<Contact />
	</div>
</template>

<script>
	import Hero from './components/Hero.vue';
	import Header from './components/Header.vue';
	import Apropos from './components/Apropos.vue';
	import Skills from './components/Skills.vue';
	import Projects from './components/Projects.vue';
	import Contact from './components/Contact.vue';
	import sal from 'sal.js';
	export default {
		name: 'App',
		components: {
			Hero,
			Header,
			Apropos,
			Skills,
			Projects,
			Contact,
		},
		mounted() {
			sal({
				threshold: 0.1,
			});
		},
	};
</script>
