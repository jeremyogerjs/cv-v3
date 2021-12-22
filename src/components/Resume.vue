<template>
    <div class="custom-section">
        <p class="text-center text-h2 pb-12 font-weight-black">Résumé</p>
        <v-row justify="center" class="mx-auto">
            
            <v-col cols="2" >
                <v-list class="custom-menu-resume">
                    <v-list-item
                        v-for="item in menuItems"
                        :key="item.title"
                        :href="item.path"
                        active-class="custom-nav"
                        :ripple="false"
                    >
                        <v-list-item-content>
                            <v-list-item-title class="font-weight-bold"> {{ item.title }} </v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-col>
            <v-col cols="7">

                <Formations  id="formations"/>

                <Experiences  id="experiences"/>

                <Skills id="competences" />

                <Awards id="recompenses" />
            </v-col>
        </v-row>
    </div>
</template>

<script>

import Awards from './sections/resume/Awards.vue'
import Experiences from './sections/resume/Experiences.vue'
import Formations from './sections/resume/Formations.vue'
import Skills from './sections/resume/Skills.vue'
export default {
    name:"Resume",
    components:{
        Awards,
        Experiences,
        Formations,
        Skills
    },
    data() {
        return {
            menuItems:[
                {title:"Formations",icon:"",path:"#formations"},
                {title:"Experiences",icon:"",path:"#experiences"},
                {title:"Compétences",icon:"",path:"#competences"},
                {title:"Récompences",icon:"",path:"#recompenses"},
            ]
        }
    }
}
</script>

<style scoped>
.custom-nav {
    color: #90ACD1;
}
.custom-menu-resume {
    position: -webkit-sticky;
    position: sticky;
    top: 100px;
}
.custom-section {
    padding: 5em 0;
}
</style>