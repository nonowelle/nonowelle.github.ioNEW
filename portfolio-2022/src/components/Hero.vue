<template>
  <section class="accueil">
    <div class="triangles show-on-scroll-right">
      <div class="un"></div>
      <div class="deux"></div>
      <div class="trois"></div>
      <div class="quatre"></div>
      <div class="cinq"></div>
    </div>
    <div class="texte show-on-scroll-left">
      <h1>
        Bonjour! <br />
        Moi, c'est <span class="nom">Marie-Ève</span>.
      </h1>
      <p class="description">
        Je suis une développeuse front-end passionnée basée à Montréal et qui a
        plus d’un tour dans son sac!
      </p>
    </div>
    <a class="rond-fleche show-on-scroll-left" v-on:click="scrollToSection">
      <i class="fas fa-arrow-down fleche" ref="fleche"></i>
    </a>
  </section>
</template>

<script>
export default {
  name: "Hero",
  methods: {
    hoverEffects() {
      //--------------BOUTON VERS À PROPOS ---------------------//
      // $(".rond-fleche").click(function () {
      //   $("html, body").animate(
      //     { scrollTop: $(".apropos").offset().top },
      //     "2000"
      //   );
      // });
    },
    scrollToSection() {
      console.log("SCROLLTOSECTION");
    },
  },
  mounted() {
    this.hoverEffects();
  },
};
</script>
