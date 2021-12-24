<template>
  <div>
    <p class="text-h4 text-sm-h3 font-weight-bold">Formations</p>
    <v-card
      v-for="(item, index) in formations"
      :key="index"
      class="pa-12 my-12 custom-hover"
      elevation="0"
      rounded="xl"
    >
      <v-row >
        <v-col
          cols="1"
          class="d-flex align-start justify-center custom-icon-mobile"
        >
          <span class="custom-icon-wrap">
            <v-icon x-large class="custom-icon-hover">mdi-school</v-icon>
          </span>
        </v-col>
        <v-col>
          <span class="font-weight-bold color-hover py-0 text-h6">
            {{ item.date }}
          </span>
          <v-card-title class="text-h5 pl-0 pt-1 font-weight-bold color-hover">
            {{ item.title }}
          </v-card-title>
          <v-card-subtitle class="color-hover pl-0">
            {{ item.place }}
          </v-card-subtitle>
        </v-col>
      </v-row>
      <v-card-text>
        <p class="text-body-1 color-hover">{{ item.content }}</p>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "FormationsAndExp",
  data() {
    return {
      formations: [
        {
          date: "2021",
          content:
            "Titre professionnel bac+2 développeur Web/mobile au CFA de la CCI.",
          title: "Formations Développeur web",
          place: "Nouméa Nouvelle Calédonie",
        },
        {
          date: "2014-2015",
          content:
            "Mention complémentaire CAP ossature bois au CFA BTP de Morcenx.",
          title: "Formations Ossature Bois",
          place: "Morcenx Aquitaine France",
        },
        {
          date: "2012-2014",
          content: "Diplôme CAP charpentier bois au CFA BTP de Morcenx.",
          title: "Formations Charpentier Bois",
          place: "Morcenx Aquitaine France",
        },
      ],
    };
  },
};
</script>

<style scoped>
.custom-hover {
    background-color: #f9f9ff;
    transition: all .3s ease-in-out;
}
.custom-hover:hover {
    background-color: #90acd1;
}
.custom-hover:hover .color-hover {
    color: white;
}
.custom-hover:hover .custom-icon-wrap{
    background-color: #f9f9ff;
}
.custom-icon-wrap {
    border-radius: 50%;
    background-color: #90acd1;
    padding: 15px;
    transition: all .3s ease-in-out;
}
.custom-icon-hover {
    color: #f9f9ff;
    transition: all .3s ease-in-out;
}
.custom-hover:hover .custom-icon-hover {
    color: #90acd1;
}
@media screen and (max-width:1030px) {
    .custom-icon-mobile {
        display: none !important;
    }
}
</style>