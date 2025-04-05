<template>
  <section id="projets" class="projects-container">
    <div class="titre">
      <h2>Mes projets</h2>
    </div>
    <div class="projects">
    <Project
      v-for="project in projects"
      :key="project.id"
      :project="project"
    />
    </div>
  </section>
</template>

<script>
import Project from './Project.vue';

export default {
  components: {
    Project,
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Mon CV',
          date: '12/03/2024',
          description: 'Voici mon CV avec mes expériences, compétences et formations',
          link: '/projets/MonCv.html',
          image: 'capture-cv.png',
          technology: 'HTML, CSS',
        },
        {
          id: 2,
          title: 'My Homespace',
          date: '12/04/2024',
          description: 'Voici la refonte d\'une page web',
          link: '/projets/MyHomespace.html',
          image: 'capture-my-homespace.png',
          technology: 'HTML, CSS',
        },
        {
          id: 3,
          title: 'Cahier des charges',
          date: '23/05/2024',
          description: 'Voici le cahier des charges pour la boutique La Socketterie',
          link: 'Cahier_des_charges_La_Socketterie.pdf',
          image: 'capture-cahier-des-charges.png',
          technology: 'Open Office',
        },
        {
          id: 4,
          title: 'Dynamisme d\'un espace de commentaire',
          date: '16/07/2024',
          description: 'Voici le dynamisme d\'un espace de commentaire',
          link: '/projets/DynamismeCommentaire.html',
          image: 'capture-dynamisme.png',
          technology: 'HTML, JS',
        },
      ],
    };
  },
};
</script>

<style scoped>
.projects-container {
  border: 1px solid white;
  background-color: #782221;
  font-size: 25px;
}

* {
  font-family: 'raleway';
}

.titre {
  border: #782221;
  text-align: center;
  padding: 20px;
}

.projects {
  border: #782221;
  display: grid;
  place-items: center;
  margin-top: 5px;
  padding-top: 5px;
  padding-bottom: 30px;
}
</style>