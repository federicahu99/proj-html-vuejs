<template>
  <div id="testimonials-section">
    <h6>happy costumers</h6>
    <h1>Testimonials</h1>
    <RoundCard :results="testimonials" id="testimonial-cards" />
  </div>
</template>

<script>
import RoundCard from "./RoundCard.vue";

export default {
  name: "TestimonialSection",
  components: {
    RoundCard,
  },
  props: {
    testimonials: Array,
  },
};
</script>

<style lang="scss" scoped >
@import "../assets/sass/style.scss";

#testimonials-section {
  margin-bottom: 130px;
  background-image: url(../assets/images/avada-movers-testimonial-background.jpg);
  background-size: cover;
  height: 748px;
  padding-top: 120px;

  h1 {
    color: $lima;
    text-transform: capitalize;
    font-weight: bold;
    margin-bottom: 80px;
    text-align: center;
  }

  #testimonial-cards {
    width: 85%;
    margin-left: 50px;
  }
}
</style>