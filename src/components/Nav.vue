<template>
  <div class="mb-16" id="home">
    <v-navigation-drawer v-model="sidebar" app temporary>
      <v-list-item
        v-for="item in items"
        :key="item.title"
        :href="item.path"
        link
        @click="sidebard = !sidebar"
      >
        <v-list-item-icon>
          <v-icon> {{ item.icon }} </v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title> {{ item.title }} </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-navigation-drawer>
    
    <v-app-bar fixed elevate-on-scroll color="white">
            <v-spacer></v-spacer>
      <v-toolbar-title class="black--text text-h5 text-sm-h5 d-flex align-center" id="me">
        <a href="#home" class="text-decoration-none black--text ">
          <v-icon color="black" x-large>mdi-color-helper</v-icon> 
          Jérémy Oger
        </a>
      </v-toolbar-title>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <v-spacer class="hidden-lg-only hidden-xl-only hidden-md-only"></v-spacer>
      <span class="hidden-lg-only hidden-xl-only hidden-md-only">
        <v-app-bar-nav-icon @click="sidebar = !sidebar"></v-app-bar-nav-icon>
      </span>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only hidden-sm-only">
        <v-btn
          color="black"
          text
          v-for="item in items"
          :key="item.title"
          :href="item.path"
        >
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
        sidebar:false,
      items: [
        { title: "Accueil", icon: "mdi-home", path: "#home" },
        { title: "Services", icon: "mdi-handshake", path: "#services" },
        { title: "A propos", icon: "mdi-pac-man", path: "#about" },
        { title: "Résumé", icon: "mdi-lan", path: "#resume" },
        {
          title: "Projets",
          icon: "mdi-trending-up",
          path: "#projets",
        },
        { title: "Contact", icon: "mdi-email", path: "#contact" },
      ],
    };
  },
};
</script>