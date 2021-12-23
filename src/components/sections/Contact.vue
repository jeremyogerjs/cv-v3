<template>
  <div class="pt-10">
    <h4
      class="text-center font-weight-black custom-border-title-section text-h3"
    >
      Travaillons ensemble
    </h4>
    <v-row class="pa-4 my-7 justify-center">
      <v-col cols="5" class="d-flex align-center black--text">
        <v-col class="mx-auto" cols="5">
          <p class="text-h5 d-flex align-center mb-6">
            <span
              class="custom-wrap-icon pa-2 d-flex align-center justify-center"
            >
              <v-icon x-large color="#90acd1">mdi-cellphone</v-icon>
            </span>
            <span class="ml-2"> 83.14.32 </span>
          </p>
          <p class="text-h5 d-flex align-center">
            <span
              class="custom-wrap-icon pa-2 d-flex align-center justify-center"
            >
              <v-icon x-large color="#90acd1">mdi-email-fast</v-icon>
            </span>
            <span class="ml-2"> jeremy.devfs@gmail.com </span>
          </p>
        </v-col>
      </v-col>
      <v-col cols="5">
        <v-form v-model="valid" @submit.prevent="sendEmail">
          <v-row class="pb-5">
            <v-col>
              <v-text-field
                v-model="email.template_params.from_name"
                type="text"
                required
                rounded
                solo
                clearable
                label="Votre nom *"
                :rules="nameRules"
                background-color="white"
                autocomplete="name"
              >
              </v-text-field>
            </v-col>
            <v-col>
              <v-text-field
                v-model="email.template_params.email"
                label="Votre email *"
                type="email"
                placeholder="example@example.com"
                required
                rounded
                clearable
                solo
                autocomplete="email"
                :rules="emailRules"
              ></v-text-field>
            </v-col>
          </v-row>
          <v-textarea
            v-model="email.template_params.message"
            label="Votre message *"
            counter
            rounded
            clearable
            solo
            :rules="contentRules"
          >
          </v-textarea>
          <v-btn color="success" :disabled="!valid" rounded type="submit">
            Envoyez un message maintenant
          </v-btn>
        </v-form>
      </v-col>
    </v-row>
    <div class="text-center ma-2">
      <v-snackbar v-model="isSend" timeout="2000">
        Votre message a bien été envoyer !
        <v-btn color="pink" text @click="isSend === false"> Fermer</v-btn>
      </v-snackbar>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Contact",
  data() {
    return {
      valid: false,
      isSend: false,
      email: {
        service_id: "service_vskznp6",
        template_id: "template_pkoisjz",
        user_id: "user_QbpDWnmz9Nav4dF6BiUHO",
        template_params: {
          from_name: "",
          email: "",
          reply_to: "Contacter par mon portfolio",
          message: "",
        },
      },
      emailRules: [
        (v) => !!v || "L'email est obligatoire",
        (v) => /.+@.+/.test(v) || "L'email doit contenir un @",
      ],
      contentRules: [
        (v) => !!v || "Veuillez mettre un message",
        (v) => v.length < 200 || "Pas plus de 200 caractéres",
      ],
      nameRules: [(v) => !!v || "Le nom est obligatoire"],
    };
  },
  methods: {
    sendEmail() {
      axios
        .post("https://api.emailjs.com/api/v1.0/email/send", this.email)
        .then((res) => {
          if (res.status == 200) {
            this.isSend === true;
          }
          console.log(res);
        })
        .catch((err) => console.log("err: ", err));
    },
  },
};
</script>

<style scoped>
.custom-wrap-icon {
  border: 3px solid #e45447;
  border-radius: 50%;
}
.custom-border-title-section {
  position: relative;
}
.custom-border-title-section::after {
  content: "";
  position: absolute;
  top: 110%;
  left: 50.5%;
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
  width: 3em;
  height: 0.05em;
}
</style>