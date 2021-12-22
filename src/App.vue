<template>
  <v-app>
    
        <Nav />

        <v-main>
          <router-view />
        </v-main>
        <Foot />
   
  </v-app>
</template>

<script>
import Nav from "@/components/Nav.vue";
import Foot from "@/components/Foot.vue";
export default {
  name: "App",
  components: {
    Nav,
    Foot,
  },
  data: () => ({
    //
  }),
};
</script>
