<template>
  <HeroArea v-if="!remove"></HeroArea>
  <!-- <button @click="changeValue">Remove from DOM</button> -->
  <Course></Course>
  <ServiceSection></ServiceSection>
  <About></About>
  <WhySection></WhySection>
  <TeamSection></TeamSection>
  <ClientSection></ClientSection>
  <InfoSection></InfoSection>
  <FooterSection></FooterSection>
</template>
<script>
import HeroArea from "@/components/HeroArea.vue";
import ServiceSection from "@/components/ServiceSection.vue";
import Course from "@/components/Course.vue";
import About from "./components/About.vue";
import InfoSection from "./components/InfoSection.vue";
import WhySection from "./components/WhySection.vue";
import TeamSection from "./components/TeamSection.vue";
import ClientSection from "./components/ClientSection.vue";
import FooterSection from "./components/FooterSection.vue";
export default {
  data() {
    return {
      remove: false,
    };
  },
  methods: {
    changeValue() {
      this.remove = !this.remove;
    },
  },
  components: {
    HeroArea,
    ServiceSection,
    Course,
    About,
    InfoSection,
    WhySection,
    TeamSection,
    ClientSection,
    FooterSection,
  },
};
</script>
