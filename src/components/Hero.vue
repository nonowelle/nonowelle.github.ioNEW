<template>
  <div class="hero" id="#hero">
    <div class="wrapper">
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
            Hello! <br />
            I'm <span class="nom">Marie-Ève</span>.
          </h1>
          <p class="description">
            I'm a French Canadian Frontend developer based in Madrid. I'm passionate about pixel-perfect beautiful interfaces and I love to add a magic touch to the internet. 
          </p>
        </div>
      </section>
      <a class="rond-fleche show-on-scroll-left" v-smooth-scroll href="#apropos">
        <i class="fas fa-arrow-down fleche" ref="fleche"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
};
</script>
