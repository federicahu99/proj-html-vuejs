<template>
  <div id="services-section" class="container">
    <h6>we are professional</h6>
    <h1>full-service solution</h1>
    <div>
      <ServiceCard :fullService="fullService"/>
    </div>
  </div>
</template>

<script>
import ServiceCard from "./ServiceCard.vue";

export default {
  name: "ServiceSection",
  components: { ServiceCard },
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
    margin-bottom: 60px;
  }

  h6 {
    color: $silver-chalice;
    text-transform: uppercase;
  }
}
</style>