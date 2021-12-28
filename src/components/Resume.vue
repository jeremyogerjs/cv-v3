<template>
  <div class="py-2 py-md-12">
    <p
      class="
        text-center text-h4 text-sm-h2
        pb-2
        custom-border-title-section
        font-weight-black
      "
    >
      Résumé
    </p>
    <v-row
      justify="center"
      class="
        mx-auto
        my-10
        flex-column flex-sm-row flex-md-row flex-lg-row flex-xl-row
      "
    >
      <v-col cols="8" sm="3" md="3" lg="3" xl="3">
        <v-list class="custom-menu-resume">
          <v-list-item
            v-for="item in menuItems"
            :key="item.title"
            :href="item.path"
            :class="{ 'v-list-item--active': item.isActive }"
            :ripple="false"
            link
            @change="navItemActive(item)"
          >
            <v-list-item-content>
              <v-list-item-title class="font-weight-bold"
                >{{ item.title }}
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
      <v-col cols="12" sm="7" md="7" lg="7" xl="7">
        <Formations id="formations" />

        <Experiences id="experiences" />

        <Skills id="competences" />

        <Awards id="recompenses" />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Awards from "./sections/resume/Awards.vue";
import Experiences from "./sections/resume/Experiences.vue";
import Formations from "./sections/resume/Formations.vue";
import Skills from "./sections/resume/Skills.vue";
export default {
  name: "Resume",
  components: {
    Awards,
    Experiences,
    Formations,
    Skills,
  },
  data() {
    return {
      menuItems: [
        { title: "Formations", icon: "", path: "#formations", isActive: false },
        {
          title: "Experiences",
          icon: "",
          path: "#experiences",
          isActive: false,
        },
        {
          title: "Compétences",
          icon: "",
          path: "#competences",
          isActive: false,
        },
        {
          title: "Récompences",
          icon: "",
          path: "#recompenses",
          isActive: false,
        },
      ],
    };
  },
  methods: {
    navItemActive(elem) {
      this.menuItems.forEach((el) => (el.isActive = false));
      elem.isActive = true;
    },
  },
};
</script>

<style scoped>
.custom-nav {
  color: #90acd1;
}
.custom-menu-resume {
  position: -webkit-sticky;
  position: sticky;
  top: 100px;
}
.v-list-item--active {
  color: #90acd1;
  background-color: transparent;
  transform: translateX(50px);
  transition: transform 0.3s ease-in-out;
}
.v-list-item {
  transition: all 0.3s ease-in-out;
}
.v-list-item--active::before {
  content: "";
  top: 45%;
  left: -10px;
  position: absolute;
  border: #90acd1 1px solid;
  height: 1px;
  width: 15px;
  transition: all 0.3s ease-in-out;
}
.v-list-item--link::before {
  top: 45%;
  left: -20px;
  position: absolute;
  border: #90acd1 1px solid;
  height: 1px;
  width: 25px;
  opacity: 0;
  transition: all 0.3s ease-in-out;
}
.custom-border-title-section {
  position: relative;
}
.custom-border-title-section::after {
  content: "";
  position: absolute;
  top: 110%;
  left: 49.9%;
  background-color: #e45447;
  border-radius: 50%;
  width: 0.25em;
  height: 0.25em;
}
.custom-border-title-section::before {
  content: "";
  position: absolute;
  top: 120%;
  left: 47%;
  background-color: #e45447;
  width: 2em;
  height: 0.05em;
}
@media screen and (max-width: 1030px) {
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 110%;
    left: 41%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 99.5%;
    left: 48.5%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.3em;
    height: 0.3em;
  }
}
@media screen and (max-width: 770px) {
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 110%;
    left: 38%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 99%;
    left: 48.5%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.3em;
    height: 0.3em;
  }
}
@media screen and (max-width: 500px) {
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 110%;
    left: 36%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 102%;
    left: 48.5%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.3em;
    height: 0.3em;
  }
}
@media screen and (max-width: 420px) {
  .custom-border-title-section::before {
    content: "";
    position: absolute;
    top: 110%;
    left: 37%;
    background-color: #e45447;
    width: 3em;
    height: 0.05em;
  }
  .custom-border-title-section::after {
    content: "";
    position: absolute;
    top: 102%;
    left: 48.3%;
    background-color: #e45447;
    border-radius: 50%;
    width: 0.3em;
    height: 0.3em;
  }
}
/**reset css vuetify */
.theme--light.v-list-item:hover::before {
  opacity: 0;
}
.theme--light.v-list-item:hover::before {
  opacity: 0;
}
.v-list-item--link:before {
  background-color: transparent;
}
.theme--light.v-list-item--active:hover::before {
  opacity: 1;
}
.theme--light.v-list-item--active::before {
  opacity: 1;
  transition: all 0.5s ease-in-out;
}
</style>