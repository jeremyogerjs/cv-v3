<template>
    <div>
        <p class="text-h3 font-weight-bold">Récompenses</p>
        <v-card
            v-for="(item,index) in awards"
            :key="index"
            class="pa-12 my-12 custom-hover"
            elevation="0"
            rounded="xl"
        >
        <v-row>
            <v-col cols="1" class="d-flex align-start justify-center">
                <span class="custom-icon-wrap"> <v-icon x-large class="custom-icon-hover">mdi-trophy-outline</v-icon> </span>
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
    name:"Awards",
    data() {
        return {
            awards:[
                {date:"2021",title:"Ocean Hackathon",content:"Arrivée en deuxième position pour la première Edition du Ocean Hackathon avec le projet WAVES.",place:"Nouméa"},
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
</style>