<template>
    <div>
        <p class="text-h4 text-sm-h3 font-weight-bold">Expériences</p>
        <v-card
            v-for="(item,index) in experiences"
            :key="index"
            class="pa-12 my-12 custom-hover"
            elevation="0"
            rounded="xl"
        >
        <v-row>
            <v-col cols="1" class="d-flex align-start justify-center custom-icon-mobile">
                <span class="custom-icon-wrap"> <v-icon x-large class="custom-icon-hover">mdi-briefcase-variant</v-icon> </span>
            </v-col>
            <v-col>
                <span class=" font-weight-bold color-hover text-h6"> 
                    {{ item.date }} 
                </span>
                <v-card-title class="text-h5 pl-0 pt-1 font-weight-bold color-hover"> {{ item.title }} </v-card-title>
                <v-card-subtitle class="color-hover pl-0 "> {{ item.place }} </v-card-subtitle>
            </v-col>
        </v-row>
            <v-card-text>
                <p class="text-body-1 color-hover"> {{ item.content }}</p>
            </v-card-text>
        </v-card>
    </div>
</template>

<script>
export default {
    name:"Experiences",
    data() {
        return {
            experiences:[
                {date:"Août/Septembre 2021",content:"Stage d'une durée d'un mois chez ISINC en travaillant sur une API en Golang.",title:"Stage",place:"ISINC"},
                {date:"Mai 2021",content:"Stage d'une durée d'un mois chez Partners Intérim en travaillant sur VueJS.",title:"Stage",place:"Partners Intérim"},
                {date:"2017-2018",content:"Poste d'ouvrier qualifé en tant que charpentier bois. J'ai travaillé sur la construction du nouveau centre culturel de Hienghène.",title:"Charpentier bois",place:"Les bois du nord"},
                {date:"2016-2017",content:"J'ai travaillé sur diverses missions tel que manoeuvre chez O.C.R, 3 mois en tant que manoeuvre chez A.E.I ou encore 3 mois comme magasinier chez Discount Teari.",title:"Intérimaire",place:"Manpower"},
            ]
        }
    }
}
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