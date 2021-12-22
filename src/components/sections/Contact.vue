<template>
    <div class="custom-bg">
        <h4 class="text-center text-h4">Travaillons ensemble</h4>
        <v-row class="pa-4">
            <v-col cols="6" class="d-flex align-center mx-auto black--text">
                <v-col class="mx-auto" cols="5">
                    <p class="text-h5">
                        <v-icon x-large color="black">mdi-phone-check</v-icon> 83.14.32
                    </p>
                    <p class="text-h5">
                        <v-icon x-large color="black">mdi-email</v-icon> jeremy.devfs@gmail.com
                    </p>
                </v-col>
            </v-col>
            <v-col cols="6">
                <v-card elevation="5" shaped>
                    <v-card-title>Contactez nous</v-card-title>
                    <v-card-text>
                    <v-form v-model="valid" @submit.prevent="sendEmail">
                        <v-text-field
                        v-model="user.email"
                            label="Votre email *"
                            type="email"
                            placeholder="example@example.com"
                            required
                            autocomplet="email"
                            prepend-icon="mdi-email"
                            :rules="emailRules"
                        ></v-text-field>
                        <v-text-field
                            v-model="user.name"
                            type="text"
                            required
                            label="Votre nom *"
                            prepend-icon="mdi-account"
                            :rules="nameRules"
                        >

                        </v-text-field>
                        <v-textarea
                            v-model="user.content"
                            label="Votre message *"
                            counter
                            prepend-icon="mdi-comment"
                            :rules="contentRules"
                            
                        >

                        </v-textarea>
                        <v-btn color="success" :disabled="!valid" type="submit">
                            Envoyez
                        </v-btn>
                    </v-form>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    name:"Contact",
    data() {
        return {
            valid:false,
            user:{
                email:"",
                name:"",
                subject:"Contacter par mon portfolio",
                content:"",
            },
            emailRules:[
                v => !!v || "L'email est obligatoire",
                v => /.+@.+/.test(v) || "L'email doit contenir un @"
            ],
            contentRules:[
                v => !!v || "Veuillez mettre un message",
                v => v.length < 200 || "Pas plus de 200 caractéres"
            ],
            nameRules:[
                v => !!v || "Le nom est obligatoire"
            ]
        }
    },
    methods: {
        sendEmail() {
            console.log(this.user);
        }
    }
}
</script>

<style scoped>
.custom-bg {
  background-color: #f9f9ff;
  padding: 2em;
}
</style>