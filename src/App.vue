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

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');


html{
  scroll-behavior: smooth;
}
.v-application {
  [class*='text-'] {
    color: #36405a;
     font-family: 'Poppins', sans-serif !important;
  }
  font-family: 'Poppins', sans-serif !important;
}
</style>
