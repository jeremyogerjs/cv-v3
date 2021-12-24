<template>
  <div>
    <p class="text-h4 text-sm-h3 font-weight-bold">Compétences</p>
    <v-row class="mt-3">
      <v-col cols="12" sm="12" md="12" lg="4" xl="4" class="d-flex align-center">
        <v-row justify="center" class="pa-2">
          <v-col cols="12" class="text-center">
             <div
              v-for="(skill, index) in skills.frontend"
              :key="index"
            >
              <div class="d-flex justify-space-between black--text">
                <p>{{ skill.title }}</p>
                <p>{{ skill.value }}%</p>
              </div>
              <v-progress-linear
                
                :value="skill.value"
                color="#90acd1"
                height="8"
                rounded
                class="mb-5"
              >
                </v-progress-linear
              >
            </div>
          </v-col>
          <v-col cols="12" sm="12" md="12" lg="4" xl="4" class="text-center">
            <div
              v-for="(skill, index) in skills.backend"
              :key="index"
            >
              <div class="d-flex justify-space-between black--text">
                <p>{{ skill.title }}</p>
                <p>{{ skill.value }}%</p>
              </div>
              <v-progress-linear
                
                :value="skill.value"
                color="#90acd1"
                height="8"
                rounded
                class="mb-5"
              >
                </v-progress-linear
              >
            </div>
          </v-col>
          <v-col cols="12" sm="12" md="12" lg="4" xl="4" class="text-center">
            <div
              v-for="(skill, index) in skills.methodologie"
              :key="index"
            >
              <div class="d-flex justify-space-between black--text">
                <p>{{ skill.title }}</p>
                <p>{{ skill.value }}%</p>
              </div>
              <v-progress-linear
                :value="skill.value"
                color="#90acd1"
                height="8"
                rounded
                class="mb-5"
              >
                </v-progress-linear
              >
            </div>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      skills: {
        frontend: [
          {
            title: "Html",
            value: 100,
            color: "brown darken-2",
            content:
              "Connaissance des meta tags(SEO) et des principales balises a connaître pour structurer correctement un site web. J'ai réalisé plusieurs petit projet pendant ma formation.",
          },
          {
            title: "Css",
            value: 90,
            color: "deep-purple accent-4",
            content:
              "Utilisation des flexboxs et librairie tiers comme vuetify,bootstrap,bulma,tailwind",
          },
          {
            title: "JS",
            value: 60,
            color: "yellow accent-2",
            content:
              "Les boucles,les tableaux,les variables,création d'algorithme,requete ajax",
          },
          {
            title: "VueJS",
            value: 60,
            color: "light-green accent-3",
            content:
              "Utilisation de vue router,vuex,toute les directives,les composants et le passage de donnée.",
          },
          {
            title: "Wordpress",
            value: 60,
            color: "deep-purple accent-4",
            content:
              "Création de théme et plugin appris en formation.Egalement l'installation de théme et plugin existant.",
          },
        ],
        backend: [
          {
            title: "PHP/POO",
            value: 80,
            color: "deep-purple accent-4",
            content:
              "Je sais créer des classes,les manipulés,notion d'héritages,les traits.",
          },
          {
            title: "Laravel",
            value: 70,
            color: "deep-orange darken-1",
            content:
              "Création rapide d'un backend migration,controller,model,relation,eloquent.Ce complète trés bien avec VueJS.",
          },
          {
            title: "SQL",
            value: 70,
            color: "yellow lighten-3",
            content:
              "Création de script de création de base de donnée.Création de script d'insertion de jeu de donnée",
          },
        ],
        methodologie: [
          {
            title: "Maquettage",
            value: 80,
            color: "cyan lighten-5",
            content:
              "Création de maquette fil de fer avec l'outil en ligne mockflow.",
          },
          {
            title: "Méthodologie Agile",
            value: 90,
            color: "cyan lighten-5",
            content:
              "Rédiger/Comprendre un cahier des charges.Utilisation de l'outil trello.Planning Poker.Daily",
          },
          {
            title: "Schéma de BDD",
            value: 90,
            color: "cyan lighten-5",
            content:
              "Création/Lecture de modèle physique de donnée et de modèle conceptuelle de donnée.",
          },
        ],
      },
    };
  },
};
</script>

<style scoped>
</style>