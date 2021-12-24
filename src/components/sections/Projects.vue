<template>
  <div class="custom-bg">
    <p
      class="
        text-center
        font-weight-black
        text-h4 text-sm-h3
        pb-5
        custom-border-title-section
      "
    >
      Mes projets
    </p>
    <v-row class="justify-center my-10 py-5">
      <v-card
        elevation="0"
        v-for="(item, index) in projects"
        :key="index"
        max-width="350px"
        min-width="250px"
        class="ma-sm-3 mb-3 custom-card-hover"
      >
        <a :href="item.path" target="_blank">
          <div class="custom-overlay"></div>
          <div class="reset-opacity">
            <v-card-title class="text-h5 white--text">
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
  padding: 5em 0;
}
.reset-opacity {
  position: absolute;
  background-color: transparent;
  opacity: 1;
  height: 100%;
  width: 100%;
  top: 90px;
  left: 5px;
  z-index: 4;
}
.custom-overlay {
  position: absolute;
  background-color: #333;
  height: 100%;
  width: 100%;
  opacity: 0.4;
  z-index: 3;
}
.custom-border-title-section {
  position: relative;
}
.custom-border-title-section::after {
  content: "";
  position: absolute;
  top: 113%;
  left: 49.5%;
  background-color: #e45447;
  border-radius: 50%;
  width: 0.25em;
  height: 0.25em;
}
.custom-border-title-section::before {
  content: "";
  position: absolute;
  top: 120%;
  left: 46%;
  background-color: #e45447;
  width: 3em;
  height: 0.05em;
}
@media screen and (max-width: 1030px) {
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 104%;
    left: 49.3%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.25em;
    height: 0.25em;
  }
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 110%;
    left: 43%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
}
@media screen and (max-width: 770px) {
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 104%;
    left: 49.3%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.25em;
    height: 0.25em;
  }
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 110%;
    left: 41%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
}
@media screen and (max-width: 500px) {
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 95%;
    left: 47%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.25em;
    height: 0.25em;
  }
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 100%;
    left: 35%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
}
@media screen and (min-width: 1400px) {
  .custom-overlay {
    position: absolute;
    background-color: transparent;
    height: 100%;
    width: 100%;
    opacity: 0;
    z-index: 2;
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
  .custom-card-hover:hover .reset-opacity {
    opacity: 1;
    color: white;
    z-index: 999;
    transform: translate(-70px, 30px);
  }
}
</style>