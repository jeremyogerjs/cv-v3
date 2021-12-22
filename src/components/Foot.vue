<template>
    <div>
        <v-footer class="pa-5">
            <v-row>
                <v-col>
                    <v-row justify="center" class="pb-5">
                        <a href="https://github.com/jeremyogerjs" class="text-decoration-none">
                            <v-icon color="black" x-large> mdi-github</v-icon>
                        </a>
                        <a href="https://www.linkedin.com/in/jeremy-oger-a78143171/" class="text-decoration-none">
                            <v-icon color="black" x-large >mdi-linkedin</v-icon>
                        </a>
                    </v-row>
                    <p class="text-center">Copyright © {{ date }} All rights reserved - Jérémy Oger</p>
                </v-col>
            </v-row>
        </v-footer>
    </div>
</template>

<script>
export default {
    name:"Foot",
    data() {
        return {
            date: "",
        }
    },

    beforeMount() {
        this.date = new Date().getFullYear();
    }
}
</script>