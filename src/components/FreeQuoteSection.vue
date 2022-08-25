<template>
  <div id="quote-section">
    <div class="container">
      <h1>request a free quote</h1>
    </div>
    <div class="container">
      <BaseForm :countries="countries" />
    </div>
  </div>
</template>

<script>
import BaseForm from "./BaseForm.vue";

export default {
  name: "FreeQuoteSection",
  components: {
    BaseForm,
  },
  props: {
    countries: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/sass/style.scss";

#quote-section {
  text-align: center;
  margin-top: 50px;
  background-image: url(../assets/images/avada-movers-request-quote-background.jpg);
  padding: 80px 0;
  margin: 0;

  h1 {
    color: $lima;
    text-transform: capitalize;
    font-weight: bold;
    margin-bottom: 50px;
    text-align: center;
  }

  p {
    width: 50%;
    margin: 0 auto;
    color: $dove-grey;
    margin-bottom: 50px;
    font-size: 15px;
  }
}
</style>