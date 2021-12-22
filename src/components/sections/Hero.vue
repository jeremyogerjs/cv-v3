<template>
    <div>
        <v-row class="justify-center align-center hero-bg" style="height:100vh">
            <v-col cols="4" >
                <span class="font-weight-bold text-h5">Hey ! Je suis</span>
                <p class="font-weight-bold text-h3">Jérémy Oger</p>
                <p>
                    <span>Je suis</span>
                    <span>Développeur frontend</span>
                </p>
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

        }
    }
}
</script>

<style scoped>
.hero-bg {
    background-color: #f9f9ff;
}
</style>