<template>
  <div>
    <v-row class="align-center justify-center py-12 custom-section-bg">
      <v-col cols="3">
        <p class="text--secondary text-uppercase">Mes services</p>
        <p class="font-weight-bold text-h4">
          Voici mes talents a votre service.
        </p>
        <p class="text--secondary">
            J'adapte mes services en fonction de vos besoins.Attentif aux nouvelles technologies, j'apporte mon expertise toujours au goût du jour.
        </p>
      </v-col>
      <v-col cols="6" class="ml-5">
        <v-row>
          <v-col cols="5" class="pa-0 mr-12">
            <v-card 
              elevation="16" 
              class="pa-12 rounded-lg text-center"
              :class="{'mt-8' : item.margin }"
              v-for="(item,index) in services1"
              :key="index"
            >
              <v-icon class="custom-icon" color="black" x-large
                > {{ item.icon }} </v-icon
              >

              <v-card-title class="justify-center"
                > {{ item.title }} </v-card-title
              >
              <v-card-subtitle
                > {{ item.subtitle }} </v-card-subtitle
              >
            </v-card>
          </v-col>
          <v-col cols="5" class="my-8 pa-0">
            <v-card 
              elevation="16" 
              class="pa-12 rounded-lg text-center"
              :class="{'mt-8' : item.margin }"
              v-for="(item,idx) in services2"
              :key="idx"
            >
              <v-icon class="custom-icon" color="black" x-large>
                {{ item.icon }}
              </v-icon>

              <v-card-title class="justify-center">
                {{ item.title }}
              </v-card-title>
              <v-card-subtitle>
                {{ item.subtitle }}  
              </v-card-subtitle
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
    return {
      services1:[
        {icon:"mdi-lightbulb-on-outline",title:"Solution adapter",subtitle:"A vos côté pendant tout le processus.",margin:false},
        {icon:"mdi-diamond-stone",title:"Développement Web",subtitle:"Développement complet de votre solution web.",margin:true},
      ],
      services2:[
        {icon:"mdi-human-capacity-decrease",title:"Performant",subtitle:"Développement rapide avec les dernières technologies.",margin:false},
        {icon:"mdi-cog-counterclockwise",title:"Maintenance",subtitle:"Votre site toujours mis a jour et sécurisé.",margin:true},
      ]
    };
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