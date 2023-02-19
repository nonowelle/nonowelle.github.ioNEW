<template>
  <div class="hero" id="#hero">
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
          Je suis une développeuse front-end québécoise basée à Madrid et qui a
          plus d’un tour dans son sac!
        </p>
      </div>
    </section>
    <a class="rond-fleche show-on-scroll-left" v-smooth-scroll href="#apropos">
      <i class="fas fa-arrow-down fleche" ref="fleche"></i>
    </a>
  </div>
</template>

<script>
export default {
  name: 'Hero',
};
</script>
