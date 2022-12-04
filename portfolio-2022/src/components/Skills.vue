<template>
  <section class="skills" id="skills">
    <h2 class="comp show-on-scroll-left">{{ title.fr }}</h2>
    <div class="container">
      <div class="show-on-scroll-right">
        <ul class="grid">
          <li v-for="link in links" :key="link.src" class="logo">
            <img :src="link.src" alt="" />
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
          src: 'imgs/express.png',
        },
        {
          src: 'imgs/MongoDB_Logo_FullColorBlack_RGB.png',
        },
        {
          src: 'imgs/sketch-symbol-transparent@2x.png',
        },
        {
          src: 'imgs/figma-1-logo-png-transparent.png',
        },
        {
          src: 'imgs/analytics.png',
        },
        {
          src: 'imgs/tag-manager.png',
        },
        {
          src: 'imgs/sitecore.png',
        },
      ],
    };
  },
};
</script>
