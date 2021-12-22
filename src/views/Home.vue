<template>
  <div>
    
      <Hero id="hero" />

      <Services id="services"/>
      
      <About id="about" />

      <Resume id="resume" />

      <Projects id="projets" />

      <Contact id="contact" />
    
    

  </div>
</template>

<script>
import Hero from "../components/sections/Hero.vue";
import Services from "../components/sections/Services.vue";
import About from "../components/sections/About.vue";
import Resume from "../components/Resume.vue";
import Projects from "../components/sections/Projects.vue";
import Contact from "../components/sections/Contact.vue";
export default {
  name: "Home",
  components: {
    About,
    Contact,
    Hero,
    Resume,
    Projects,
    Services
  },
};
</script>
