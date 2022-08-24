<template>
  <div id="services-section" class="_container">
    <h5>we are professional</h5>
    <h1>full-service solution</h1>
    <div>
      <RectangularCard :results="fullService"/>
    </div>
  </div>
</template>

<script>
import RectangularCard from "./RectangularCard.vue";

export default {
  name: "ServiceSection",
  components: { RectangularCard },
  props: {
    fullService: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#services-section {
  padding-top: 100px;
  text-align: center;

  h1 {
    color: $lima;
    text-transform: capitalize;
    font-weight: bold;
    margin-bottom: 80px;
  }

  h5 {
    color: $silver-chalice;
    text-transform: uppercase;
  }
}
</style>