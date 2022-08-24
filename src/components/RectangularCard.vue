<template>
  <div class="d-flex row g-lg-2" id="card-section">
    <div
      class="card d-flex offset-lg-1 col-lg-3"
      v-for="(result, i) in results"
      :key="i"
    >
      <figure>
        <img :src="GetImagine(result)" :alt="`${result.title}photo`" class="img-fluid" />
      </figure>
      <div class="bg-white">
        <h3>{{ result.title  }}</h3>
        <div class="card-text">
          {{ result.text}}
        </div>
        <BaseButton :text="result.btn" class="m-4" />
      </div>
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "BaseCard",
  props: {
    results: Array,
  },
  components: { BaseButton },
  methods: {
    GetImagine(result) {
      return require(`../assets/images/${result.img}`); // img path method
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
  text-align: center;
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
    text-align: center;
  }

}
</style>