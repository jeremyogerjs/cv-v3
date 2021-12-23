<template>
    <div>
        <v-row class="justify-center align-center hero-bg" style="height:100vh">
            <v-col cols="4">
                <span class="font-weight-bold text-h5 custom-color">Hey ! Je suis</span>
                <p class="font-weight-bold text-h2">Jérémy Oger !</p>
                <v-row class="align-center py-4">
                    <span class="text-body-1 mr-2 custom-color-hero">Je suis </span>
                    <span class="animate d-inline-block custom-color-hero text-h5"> {{ titleShow }}</span>
                </v-row>
                <p class="text--secondary">
                    Dorem ipsum dolor sitamet, consectetur adipiscing elit, 
                    sed do eiusm tempor incididunt ulabore et dolore magna aliqua.
                </p>
            </v-col>
            <v-col cols="4">
                <div>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi sint officia voluptas, rem voluptatibus reprehenderit nostrum numquam nulla quam accusamus excepturi alias consectetur assumenda vitae sapiente officiis ab quidem perspiciatis?</p>
                </div>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    name:"Hero",
    data() {
        return {
            title:[
                "Développeur frontend",
                "Développeur backend",
                "Développeur freelance"
            ],
            titleShow:"Développeur frontend",
            interval:0,
        }
    }, 
    mounted: function(){
        let i = 0;
        this.stopInterval();
        this.interval = setInterval(() => {
                this.titleShow = this.title[i++];
               if(i == this.title.length) i=0 
            },7200)
    },
    methods:{
        stopInterval() {
            clearInterval(this.interval);
            
        }
    }
}
</script>

<style scoped lang="css">
.hero-bg {
    background-color: #f9f9ff;
}
.custom-width-title {
    width: max-content;
}
.custom-color {
    color: #90acd1;
}
.custom-color-hero {
    color: #e45447;
}
.animate {
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .15em solid #e45447; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  letter-spacing: .15em; /* Adjust as needed */
  max-width: fit-content;
  animation: 
    typing 3.5s steps(40, end) infinite alternate,
    blink-caret .75s step-end infinite;
}

/* The typing effect */
@keyframes typing {
  from { width: 0% }
  to { width: 100% }
}
/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: #e45447; }
}
</style>