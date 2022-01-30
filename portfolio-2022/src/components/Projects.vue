<template>
  <section class="projets" id="projets">
    <h2 class="show-on-scroll-left">Mes projets</h2>
    <div class="planties">
      <img
        class="projets-img show-on-scroll-left"
        src="imgs/planties.png"
        alt="captures-ecran-pages-web"
      />
      <div class="planties-texte show-on-scroll-right">
        <h3>Planties</h3>
        <p>
          Planties est ma première application Web complète. Créez-vous un
          compte et vous pourrez collectionner et partager des photos de vos
          plantes avec d'autres passionnés. Elle est inspirée du projet Yelpcamp
          du cours The Web Developper Bootcamp (par Colt Steele). Grâce à ce
          projet, j'ai appris à utiliser Express, Node.js et MongoDB.
        </p>

        <p>
          Technologies utilisées :
          <span class="tech"
            >Bootstrap - Express - Node.js - MongoDB - EJS
          </span>
        </p>
        <div class="btn">
          <a
            target="_blank"
            href="https://serene-caverns-99636.herokuapp.com/"
            class="site"
            >Site Web <i class="fas fa-long-arrow-alt-right lien"></i
          ></a>
        </div>
        <div class="btn" type="button">
          <a
            target="_blank"
            href="https://github.com/nonowelle/planties"
            class="site"
            >Code <i class="fas fa-long-arrow-alt-right lien"></i
          ></a>
        </div>
      </div>
    </div>
    <div class="crism">
      <div class="crism-texte show-on-scroll-left">
        <h3>CRISM</h3>
        <p>
          À titre d'édimestre pour l'<em
            >Initiative canadienne de recherche en abus de substances </em
          >(CRISM), j'avais pour mandat de procéder à la refonte du visuel et du
          contenu du site Web de l'organisation. Je devais utiliser le thème
          Wordpress mis en place lors de la création du site, Jupiter 6. J'ai
          donc créé une nouvelle arborescence, établi une nouvelle palette de
          couleurs et créé des maquettes avec Figma pour finalement mettre en
          place le nouveau design. J'ai également procédé à l'ajout de
          métadecriptions via le plugin Yoast pour améliorer le référencement
          naturel.
        </p>
        <p>
          Technologies utilisées :
          <span class="tech"
            >Wordpress - Thème Jupiter 6 - CSS - YoastSEO - Figma
          </span>
        </p>
        <div class="btn">
          <a
            target="_blank"
            href="https://www.crismquebecatlantic.ca/"
            class="site"
            >Site Web <i class="fas fa-long-arrow-alt-right lien"></i
          ></a>
        </div>
      </div>
      <img
        class="show-on-scroll-right projets-img show-on-scroll"
        src="imgs/CRISM.png"
        alt="captures-ecran-pages-web"
      />
    </div>

    <div class="landing">
      <div class="landing-texte show-on-scroll-right">
        <h3>Page FAQ</h3>
        <p>
          Ce projet constitue mon troisième défi de Front-End Mentor Challenge.
          Il s'agit d'une section <em>Questions fréquentes</em> sous forme
          d'accordéon. Je devais reproduire le plus fidèlement possible le
          design qui m'avait été fourni en utilisant les outils de mon choix.
          Mon design devait être responsive et s'adapter à tous les navigateurs.
        </p>
        <p>
          Technologies utilisées :
          <span class="tech">HTML - CSS - Vanilla JS </span>
        </p>
        <div class="btn">
          <a
            target="_blank"
            href="https://faq-accordion-card-challenge-git-main.nonowelle.vercel.app/"
            class="site"
            >Site Web <i class="fas fa-long-arrow-alt-right lien"></i
          ></a>
        </div>
        <div class="btn" type="button">
          <a
            target="_blank"
            href="https://github.com/nonowelle/faq-accordion-card-challenge"
            class="site"
            >Code <i class="fas fa-long-arrow-alt-right lien"></i
          ></a>
        </div>
      </div>
      <img
        class="projets-img show-on-scroll-left"
        src="/imgs/accordion.png"
        alt=""
      />
    </div>
  </section>
</template>

<script>
export default {
  name: "Projects",
};
</script>
