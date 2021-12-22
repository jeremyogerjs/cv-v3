<template>
  <div>
    <v-row class="align-center justify-center py-12 custom-section-bg">
      <v-col cols="3">
        <p class="text--secondary text-uppercase">Mes services</p>
        <p class="font-weight-bold text-h4">
          Voici mes talents a votre service.
        </p>
        <p class="text--secondary">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorem
          omnis facere beatae harum quis eaque natus quas iusto, perferendis
          velit quisquam error alias, sit nisi impedit nobis, veniam provident
          eum.
        </p>
      </v-col>
      <v-col cols="6" class="ml-5">
        <v-row>
          <v-col cols="5" class="pa-0 mr-12">
            <v-card elevation="16" class="pa-12 rounded-lg text-center">
              <v-icon class="custom-icon" color="black" x-large
                >mdi-lightbulb-on-outline</v-icon
              >

              <v-card-title class="justify-center"
                >Solution adapter</v-card-title
              >
              <v-card-subtitle
                >A vos côté pendant tout le processus.</v-card-subtitle
              >
            </v-card>
            <v-card elevation="16" class="pa-12 mt-8 rounded-lg text-center">
              <v-icon class="custom-icon" color="black" x-large
                >mdi-lightbulb-on-outline</v-icon
              >

              <v-card-title class="justify-center"
                >Web Développement</v-card-title
              >
              <v-card-subtitle
                >Développement complet de votre solution web.</v-card-subtitle
              >
            </v-card>
          </v-col>
          <v-col cols="5" class="my-8 pa-0">
            <v-card elevation="16" class="pa-12 rounded-lg text-center">
              <v-icon class="custom-icon" color="black" x-large
                >mdi-lightbulb-on-outline</v-icon
              >

              <v-card-title class="justify-center"></v-card-title>
              <v-card-subtitle
                >Développement complet de votre solution web.</v-card-subtitle
              >
            </v-card>
            <v-card elevation="16" class="pa-12 mt-8 rounded-lg text-center">
              <v-icon class="custom-icon" color="black" x-large
                >mdi-lightbulb-on-outline</v-icon
              >

              <v-card-title class="justify-center"
                >Web Développement</v-card-title
              >
              <v-card-subtitle
                >Développement complet de votre solution web.</v-card-subtitle
              >
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Services",
  data() {
    return {};
  },
};
</script>

<style scoped>
.custom-icon {
  padding: 18px;
  background-color: #f9f9f9;
  border-radius: 10px;
  
}
.custom-section-bg {
  background-image: url("../../assets/bg-half.png");
  background-repeat: no-repeat;
  background-position: top right;
  background-size: 60%;
  margin-top: 4em;
}
</style>