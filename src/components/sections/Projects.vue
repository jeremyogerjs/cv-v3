<template>
  <div class="custom-bg">
    <p class="text-center font-weight-black text-h3">Mes projets</p>
    <v-row class="justify-center">
      <v-card
        elevation="0"
        v-for="(item, index) in projects"
        :key="index"
        width="400px"
        class="ma-3 custom-card-hover"
      >
        <a :href="item.path" target="_blank">
          <div class="custom-overlay"></div>
          <div class="reset-opacity">
            <v-card-title class="text-h5 white-text">
              {{ item.type }}
            </v-card-title>
            <v-card-text>
              <v-chip
                v-for="(language, idx) in item.languages"
                :key="idx"
                class="mr-2"
                color="#f9f9ff"
              >
                {{ language }}
              </v-chip>
            </v-card-text>
          </div>
        </a>
        <v-img src="../../assets/bg-projects.jpg" height="200px"> </v-img>
      </v-card>
    </v-row>
  </div>
</template>


<script>
export default {
  name: "Projects",
  data() {
    return {
      projects: [
        {
          type: "Ecommerce",
          path: "",
          languages: ["vueJS", "Laravel", "MySQL"],
        },
        {
          type: "Réservations",
          path: "efef",
          languages: ["VueJS", "Laravel", "MySQL"],
        },
        {
          type: "Appli mobile",
          path: "",
          languages: ["React Navtive", "Laravel", "MySQL"],
        },
        { type: "Blog", path: "fefe", languages: ["Wordpress", "MySQL"] },
      ],
    };
  },
};
</script>

<style scoped>
.custom-bg {
  background-color: #f9f9ff;
  padding: 2em;
}
.custom-overlay {
  position: absolute;
  background-color: transparent;
  height: 100%;
  width: 100%;
  opacity: 0;
  z-index: 30;
  transition: all 0.3s ease-in-out;
}
.custom-card-hover:hover .custom-overlay {
  background-color: #e45447;
  transform: translate(20px, 20px);
  opacity: 0.9;
  cursor: pointer;
}
.reset-opacity {
    position: absolute;
    opacity: 0;
    height: 100%;
    width: 100%;
    top: 55px;
    left: 110px;
    transition: all 0.3s ease-in-out;
}
.custom-card-hover:hover .reset-opacity 
{
    opacity: 1;
    color: white;
    z-index: 999;
    transform: translate(-70px,30px);
}
</style>