<template>
  <section class="projets" id="projets">
    <h2 class="show-on-scroll-left">Mes projets</h2>
    <li v-for="(project, index) in projects" :key="project.id">
      <div
        class="project-details"
        :class="{
          'show-on-scroll-left': index % 2 === 0,
          'show-on-scroll-right': index % 2 !== 0,
        }"
      >
        <img :src="project.img" alt="" />
        <div class="project-text">
          <h3>{{ project.title }}</h3>
          <p class="project-description">{{ project.description }}</p>
          <div>
            <p>Technologies utilisées :</p>
            <span class="tech"
              ><li v-for="tech in project.techs" :key="tech.id" class="techs">
                {{ tech }}
              </li></span
            >
          </div>

          <div class="btn">
            <a target="_blank" :href="project.links[0]" class="site"
              >Site Web <i class="fas fa-long-arrow-alt-right lien"></i
            ></a>
          </div>
          <div v-if="project.links[1]" class="btn">
            <a target="_blank" :href="project.links[1]" class="site"
              >Code <i class="fas fa-long-arrow-alt-right lien"></i
            ></a>
          </div>
        </div>
      </div>
    </li>
  </section>
</template>

<script>
export default {
  name: 'Projects',
  data: function () {
    return {
      projects: [
        {
          id: 1,
          title: 'Planties',
          description:
            "Planties est ma première application Web complète. Créez-vous un compte et vous pourrez collectionner et partager des photos de vos plantes avec d'autres passionnés. Elle est inspirée du projet Yelpcamp du cours The Web Developper Bootcamp (par Colt Steele). Grâce à ce projet, j'ai appris à utiliser Express, Node.js et MongoDB.",
          img: 'imgs/planties.png',
          techs: [
            { name: 'Bootstrap', id: 1 },
            { id: 2, name: 'Express' },
            { id: 3, name: 'Node.js' },
            { id: 4, name: 'MongoDB' },
            { id: 5, name: 'EJS' },
          ],
          links: [
            'https://serene-caverns-99636.herokuapp.com/',
            'https://github.com/nonowelle/planties',
          ],
        },
        {
          id: 2,
          title: 'CRISM',
          description:
            "À titre d'édimestre pour l'<em>Initiative canadienne de recherche en abus de substances </em>(CRISM), j'avais pour mandat de procéder à la refonte du visuel et du contenu du site Web de l'organisation. Je devais utiliser le thème Wordpress mis en place lors de la création du site, Jupiter 6. J'ai donc créé une nouvelle arborescence, établi une nouvelle palette de couleurs et créé des maquettes avec Figma pour finalement mettre en place le nouveau design. J'ai également procédé à l'ajout de métadecriptions via le plugin Yoast pour améliorer le référencement naturel.",
          img: 'imgs/CRISM.png',
          techs: [
            { name: 'Wordpress', id: 1 },
            { name: 'Thème Jupiter 6', id: 2 },
            { name: 'CSS', id: 3 },
            { name: 'YoastSEO', id: 4 },
            { name: 'Figma', id: 5 },
          ],
          links: ['https://www.crismquebecatlantic.ca/'],
        },
        {
          id: 3,
          title: 'Page FAQ',
          description:
            "Ce projet constitue mon troisième défi de Front-End Mentor Challenge. Il s'agit d'une section <em>Questions fréquentes</em> sous forme d'accordéon. Je devais reproduire le plus fidèlement possible le design qui m'avait été fourni en utilisant les outils de mon choix. Mon design devait être responsive et s'adapter à tous les navigateurs.",
          img: '/imgs/accordion.png',
          techs: [
            { name: 'HTML', id: 1 },
            { name: 'CSS', id: 2 },
            { name: 'Vanilla JS', id: 3 },
          ],
          links: [
            'https://faq-accordion-card-challenge-git-main.nonowelle.vercel.app/',
            'https://github.com/nonowelle/faq-accordion-card-challenge',
          ],
        },
      ],
    };
  },
};
</script>
