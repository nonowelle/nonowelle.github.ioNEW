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
  methods: {
    scrollEffects() {
      let scroll =
        window.requestAnimationFrame ||
        function (callback) {
          window.setTimeout(callback, 1000 / 60);
        };

      let elementsToShow = document.querySelectorAll('.show-on-scroll-left');

      function loopL() {
        elementsToShow.forEach(function (element) {
          if (isElementInViewport(element)) {
            element.classList.add('is-visible-left');
          } else {
            element.classList.remove('is-visible-left');
          }
        });
        scroll(loopL);
      }

      loopL();

      let elementsToShowRight = document.querySelectorAll(
        '.show-on-scroll-right'
      );

      function loopR() {
        elementsToShowRight.forEach(function (element) {
          if (isElementInViewport(element)) {
            element.classList.add('is-visible-right');
          } else {
            element.classList.remove('is-visible-right');
          }
        });
        scroll(loopR);
      }

      loopR();

      function isElementInViewport(el) {
        var rect = el.getBoundingClientRect();
        return (
          (rect.top <= 0 && rect.bottom >= 0) ||
          (rect.bottom >=
            (window.innerHeight || document.documentElement.clientHeight) &&
            rect.top <=
              (window.innerHeight || document.documentElement.clientHeight)) ||
          (rect.top >= 0 &&
            rect.bottom <=
              (window.innerHeight || document.documentElement.clientHeight))
        );
      }
    },
  },
  mounted() {
    this.scrollEffects();
  },
};
</script>
