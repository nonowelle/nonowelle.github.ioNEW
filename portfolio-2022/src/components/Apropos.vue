<template>
  <div class="apropos" id="apropos">
    <h2 class="titre-apropos show-on-scroll-left">{{ title }}</h2>
    <p class="para show-on-scroll-left">
      {{ texte }}
    </p>

    <div class="btn cv show-on-scroll-left">
      <a target="_blank" href="./imgs/CV-2021.pdf" download="CV-MENoel"
        ><b>CV</b> <i class="fas fa-long-arrow-alt-right lien"></i
      ></a>
    </div>
    <div class="parcours">
      <div class="etudes">
        <div class="entries">
          <ul>
            <li
              v-for="(entry, index) in entries"
              :key="entry.title"
              :class="{
                'show-on-scroll-left': index % 2 === 0,
                'show-on-scroll-right': index % 2 !== 0,
              }"
              class="entry"
            >
              <p class="title">{{ entry.title }}</p>
              <div class="desc">
                <ul>
                  <li v-for="job in entry.jobs" :key="job.jobTitle">
                    <div class="desc">
                      <p class="job-title">{{ job.jobTitle }}</p>
                      <p class="job-desc">{{ job.jobDesc }}</p>
                    </div>
                  </li>
                </ul>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Apropos',
  data() {
    return {
      title: 'À propos',
      texte:
        "Avant de me lancer dans le développement front-end, j'ai évolué dans le domaine des langues et du marketing. J'ai une passion pour les langages, qu'ils soient linguistiques ou informatiques. Grâce à eux, non seulement je peux communiquer, mais je peux maintenant donner vie à des designs Web élégants et responsive. Envie d'en savoir plus?",
      entries: [
        {
          title: "mai 2021 à aujourd'hui",
          jobs: [
            {
              jobTitle: 'Front-End Developer - Coveo',
              link: 'https://www.coveo.com/',
              jobDesc: 'Design - CSS - JS - Vue - GTM - Figma',
            },
          ],
        },
        {
          title: '2020',
          jobs: [
            {
              jobTitle: 'Webmaster - CRISM',
              link: 'https://www.crismquebecatlantic.ca/',
              jobDesc:
                'Intégration Wordpress - Design - SEO- Rédaction - Gestion de contenu',
            },

            {
              jobTitle: 'The Modern Javascript Bootcamp',
              link: 'https://www.udemy.com/course/javascript-beginners-complete-tutorial/',
              jobDesc: 'En cours',
            },
            {
              jobTitle: 'The Web Developer Bootcamp 2020 Certification',
              link: 'https://www.udemy.com/course/the-web-developer-bootcamp/',
              jobDesc: 'Complété',
            },
          ],
        },
        {
          title: '2019',
          jobs: [
            {
              jobTitle: 'DESS en Gestion - ESG',
            },
          ],
        },
        {
          title: '2018-2019',
          jobs: [
            {
              jobTitle: ' Agente au marketing - Druide informatique',
              link: 'www.druide.com',
              jobDesc:
                'SEO - Marketing numérique - Intégration Web - Gestion des commandites - Rédaction',
            },
          ],
        },
        {
          title: '2016',
          jobs: [
            {
              jobTitle: 'Maîtrise études hispaniques',
            },
          ],
        },
      ],
    };
  },
};
</script>
