<template>
  <div class="d-flex row" id="card-section">
    <div
      class="testimonial-card col-6 col-md-4 "
      v-for="(result, i) in results"
      :key="i"
    >
      <figure class="d-flex justify-content-center" id="container-img-testimonial">
        <img :src="GetImagine(result)" :alt=" `${result.nameLastname}photo`" />
      </figure>
      <div>
        <h3>{{ result.nameLastname  }}</h3>
        <p><cite class="card-text">
          {{ result.text }}
        </cite></p>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "BaseCard",
  props: {
    results: Array,
  },
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

.testimonial-card {

  .card-text {
    margin: 10px 0;
    padding: 0 20px;
    line-height: 200%;
    font-size: 10px;
    color: $dove-grey;
    text-align: center
  }

  img {
    border-radius: 50%;
    width: 40%;
  }

  #container-img-testimonial {
    background-color: none;
  }

}
</style>