<template>
  <HeroArea v-if="!remove"></HeroArea>
  <button @click="changeValue">Remove from DOM</button>
  <Course></Course>
  <ServiceSection></ServiceSection>
</template>
<script>
import HeroArea from "@/components/HeroArea.vue";
import ServiceSection from "@/components/ServiceSection.vue";
import Course from "@/components/Course.vue";
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
  },
};
</script>
