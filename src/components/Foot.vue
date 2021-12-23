<template>
    <div>
        <v-footer class="py-12">
            <v-row>
                <v-col>
                    <v-row justify="center" class="pb-5">
                        <v-hover v-slot="{ hover }">
                            <a href="https://github.com/jeremyogerjs" target="_blank" class="text-decoration-none custom-hover-social">
                                <v-icon :color=" hover ? 'red' : 'black'" class="custom-hover-social" x-large> mdi-github</v-icon>
                            </a>
                        </v-hover>
                        <v-hover v-slot="{ hover }">
                            <a href="https://www.linkedin.com/in/jeremy-oger-a78143171/" target="_blank" class="text-decoration-none">
                                <v-icon :color="hover ? 'red' : 'black'" x-large >mdi-linkedin</v-icon>
                            </a>
                        </v-hover>
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