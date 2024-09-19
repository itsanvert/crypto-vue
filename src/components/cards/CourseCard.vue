<template>
  <div class="col-md-4">
    <div class="box">
      <div class="detail-box">
        <h5>{{ title }}</h5>
        <p>{{ price }}</p>
        <p>
          {{ shortDescription }}
        </p>
        <a href=""> Read More </a>
      </div>
    </div>
  </div>
</template>
  <script>
export default {
  props: ["title", "shortDescription", "price"],
};
</script>