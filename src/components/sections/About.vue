<template>
  <div class="custom-bg">
    <v-row class="mt-0" justify="center">
      <v-col cols="5" class="d-flex align-center" style="height: 60vh">
        <v-img
            max-width="55vh"
          contain
          alt="photo de moi sur montagne"
          src="../../assets/photo_profil.jpg"
        ></v-img>
      </v-col>
      <v-col cols="5">
        <p class="text-h3 font-weight-bold pb-5">A propos de moi</p>
        <p class="text--secondary text-body-1 pb-5">
            Je suis diplomé d'un bac+2 en développement web et mobile. Spécialisé dans le développement mdoerne d'application web et mobile.
        </p>

            <ul class="custom-ul pb-8">
                <li class="d-flex align-center "> 
                    <span class="font-weight-bold text-button custom-li">Nom: </span>
                    <span class="text-body-1 text--secondary">Oger Jérémy</span>
                </li>
                <li class="d-flex align-center">
                    <span class="font-weight-bold text-button custom-li">Date de naissance: </span>
                    <span class="text-body-1 text--secondary">06/05/1996</span>
                </li>
                <li class="d-flex align-center">
                    <span class="font-weight-bold text-button custom-li">Adresse: </span>
                    <span class="text-body-1 text--secondary">31 route des phoenix</span>
                </li>
                <li class="d-flex align-center">
                    <span class="font-weight-bold text-button custom-li">Code postal: </span>
                    <span class="text-body-1 text--secondary">98830 Dumbéa - Auteuil</span>
                </li>
                <li class="d-flex align-center">
                    <span class="font-weight-bold text-button custom-li">Email:</span>
                    <span class="text-body-1 text--secondary">jeremy.devfs@gmail.com</span>
                </li>
                <li class="d-flex align-center">
                    <span class="font-weight-bold text-button custom-li">Téléphone: </span>
                    <span class="text-body-1 text--secondary">(+687) 83.14.32</span>
                </li>
            </ul>

        <v-row class="justify-space-around">
          <v-btn
            href="https://github.com/jeremyogerjs"
            color="purple darken-1"
            target="_blank"
          >
            <v-icon>mdi-github</v-icon>
            Github
          </v-btn>
          <v-btn
            href="https://www.linkedin.com/in/jeremy-oger-a78143171/"
            color="blue lighten-1"
            target="_blank"
          >
            <v-icon>mdi-linkedin</v-icon>
            LinkedIn
          </v-btn>
          <v-btn
            href="https://www.linkedin.com/in/jeremy-oger-a78143171/"
            color="white"
            target="_blank"
          >
            <v-icon>mdi-download</v-icon>
            Télécharger mon CV
          </v-btn>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {};
  },
};
</script>

<style scoped>
.custom-bg {
  background-color: #f9f9ff;
  padding:2em;
}
.custom-li{
    width: 180px;
    padding:.3em;
}
.custom-ul {
    list-style: none;
    padding-left: 0;
}
</style>