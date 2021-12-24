<template>
  <div>
    <v-row class="justify-sm-center align-center hero-bg" style="height: 100vh">
      <v-col cols="10" sm="9" lg="4" xl="4" class="custom-mobile-hero">
        <span class="font-weight-bold text-h5 custom-color">Hey ! Je suis</span>
        <p class="font-weight-bold text-h2">Jérémy Oger !</p>
        <v-row class="align-center py-4">
          <span class="text-body-1 mr-2 custom-color-hero">Je suis </span>
            <span class="animate custom-color-hero text-h6">
                {{ titleShow }}</span
            >
        </v-row>
        <p class="text--secondary">
          Dorem ipsum dolor sitamet, consectetur adipiscing elit, sed do eiusm
          tempor incididunt ulabore et dolore magna aliqua.
        </p>
      </v-col>
      <v-col
        cols="9"
        sm="9"
        lg="4"
        xl="4"
        class="hidden-sm-only hidden-md-only hidden-xs-only"
      >
        <div>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi
            sint officia voluptas, rem voluptatibus reprehenderit nostrum
            numquam nulla quam accusamus excepturi alias consectetur assumenda
            vitae sapiente officiis ab quidem perspiciatis?
          </p>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {
      title: [
        "Développeur frontend",
        "Développeur backend",
        "Développeur freelance",
      ],
      titleShow: "Développeur frontend",
      interval: 0,
    };
  },
  mounted: function () {
    let i = 0;
    this.stopInterval();
    this.interval = setInterval(() => {
      this.titleShow = this.title[i++];
      if (i == this.title.length) i = 0;
    }, 2500);
  },
  methods: {
    stopInterval() {
      clearInterval(this.interval);
    },
  },
};
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
  letter-spacing: 0.15em; /* Adjust as needed */
  max-width: fit-content;
  animation: slideY 2.5s linear infinite;
}
@keyframes slideY {
    0%{
        transform:translateY(20px);
        opacity: 0;
    }
    50%{
        opacity: 1;
    }
    100% {
        transform: translateY(-20px);
        opacity: 0;
    }
}
@media screen and (max-width: 600px) {
  .custom-mobile-hero {
    margin: 0 auto;
  }
}
</style>