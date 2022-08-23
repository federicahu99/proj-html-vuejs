<template>
  <div class="d-flex">
    <div class="card" v-for="(service, i) in fullService" :key="i">
      <figure>
        <img
          :src="GetImagine(service)"
          :alt="`${service.title} photo`"
        />
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
      return require(`../assets/images/${service.img}`); // img path
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
  padding: 15px;
  margin: 10px;
  background-color: $mercury;
  border-radius: 5px;

  .card-text {
    margin: 15px 0;
    padding: 20px;
  }

  img{
       width: 100%;
  }
}
</style>