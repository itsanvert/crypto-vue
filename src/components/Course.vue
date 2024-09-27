<template>
  <section class="service_section layout_padding">
    <div class="service_container">
      <div class="container">
        <div class="heading_container heading_center">
          <h2>Our <span>Courses</span></h2>
          <p>
            There are many variations of passages of Lorem Ipsum available, but
            the majority have suffered alteration
          </p>
        </div>
        <div class="row">
          <CourseCard
            v-for="(course, index ) in courses"
            :key="index"
            :title="course.title"
            :short-description="course.shortDescription"
            :price="course.price"
          ></CourseCard>
          
        </div>
        <div class="btn-box">
          <a href=""> View All </a>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import CourseCard from "@/components/cards/CourseCard.vue";
import axios from "axios";
export default {
  components: { CourseCard },
  data() {
    return {
      courses: [],
    };
  },
  async created() {
    const data = "";
    const response = await axios.get("/v1/courses");
    this.courses = response.data;
    console.log(this.courses);
  },
};
</script>