<template>
  <div class="d-flex row g-lg-2" id="card-section">
    <div
      class="card d-flex offset-lg-1 col-lg-3"
      v-for="(service, i) in fullService"
      :key="i"
    >
      <figure>
        <img :src="GetImagine(service)" :alt="`${service.title} photo`" />
      </figure>
      <div class="bg-white">
        <h3>{{ service.title }}</h3>
        <div class="card-text">
          {{ service.text }}
        </div>
        <BaseButton :text="service.btn" class="m-4" />
      </div>
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "ServiceCard",
  props: {
    fullService: Array,
  },
  components: { BaseButton },
  methods: {
    GetImagine(service) {
      return require(`../assets/images/${service.img}`); // img path method
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/style.scss";

h3 {
  text-transform: capitalize;
  color: $denim;
  margin: 15px 0;
  font-weight: bold;
}

h6 {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: bold;
  color: $dove-grey;
  margin-top: 150px;
}

.card {
  padding: 10px;
  margin-bottom: 160px;
  background-color: $mercury;
  border-radius: 5px;

  .card-text {
    margin: 10px 0;
    padding: 0 20px;
    line-height: 200%;
    font-size: 12px;
    color: $dove-grey;
  }

  img {
    width: 100%;
  }
}
</style>