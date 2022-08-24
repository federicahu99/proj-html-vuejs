<template>
  <div id="testimonials-section">
    <div class="container">
      <h6>happy costumers</h6>
      <h1>Testimonials</h1>
      <RoundCard :results="testimonials" class="testimonial-cards" />
      <BaseButton text="READ MORE TESTIMONIAL" />
    </div>
  </div>
</template>

<script>
import RoundCard from "./RoundCard.vue";
import BaseButton from "./BaseButton.vue";

export default {
  name: "TestimonialSection",
  components: {
    RoundCard,
    BaseButton,
  },
  props: {
    testimonials: Array,
  },
};
</script>

<style lang="scss" scoped >
@import "../assets/sass/style.scss";

#testimonials-section {
  width: 100%;
  margin-bottom: 50px;
  background-image: url(../assets/images/avada-movers-testimonial-background.jpg);
  background-size: cover;
  padding-top: 80px;
  text-align: center;

  h1 {
    color: $lima;
    text-transform: capitalize;
    font-weight: bold;
    margin-bottom: 30px;
  }
}
</style>