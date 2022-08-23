<template>
  <div id="services-section" class="container">
    <h6>we are professional</h6>
    <h1>full-service solution</h1>
    <div class="card">
      <figure v-for="(service, i) in fullService" :key="i">
        <img src="GetImagine" alt="service.name" />
      </figure>
      <h3>{{ service.name }}</h3>
      <div>
        {{ service.text }}
      </div>
      <BaseButton text="service.bnt" />
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "ServicesSection",
  components: { BaseButton },
  props: {
    fullService: Object,
  },
  computed: {
    GetImagine() {
      return `../../assets/images/${this.service.img}`;
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

h6 {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: bold;
  color: $dove-grey;
  margin-top: 150px;
}

h1 {
  text-transform: uppercase;
  font-weight: bold;
  color: $lima;
  margin-top: 30px;
}
</style>