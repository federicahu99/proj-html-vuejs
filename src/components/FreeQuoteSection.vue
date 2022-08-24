<template>
  <div id="quote-section">
    <div class="container">
      <h1>request a free quote</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, esse saepe
        quo, fugiat tempora odit accusantium maiores dolores omnis quam sint
        assumenda dignissimos blanditiis consectetur delectus exercitationem
        distinctio labore doloremque!
      </p>
      <BaseButton text="CLICK HERE" id="button-quote" />
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "FreeQuoteSection",
  components: {
    BaseButton,
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