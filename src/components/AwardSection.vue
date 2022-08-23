<template>
  <div id="award-section">
    <div class="container" id="smaller-container">
      <h6>headache free</h6>
      <h1>
        award winning <br />
        moving company
      </h1>
      <div id="award-text">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam
        debitis laudantium assumenda quam repellat repellendus praesentium, a,
        neque tempore harum aspernatur. Illo sapiente tempore exercitationem
        cumque amet unde dolorem!
      </div>
      <!-- Prop for button in award section-->
      <BaseButton text="read our testimonials" id="testimonial-award-section"/>
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";

export default {
  name: "AwardSection",
  components: {
    BaseButton,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#award-section {
  height: 660px;
  background-color: $mercury;
  padding: 140px 0;

  #smaller-container {
    width: 75%;
    text-align: center;
  }

  #award-text {
    color: $dove-grey;
    line-height: 200%;
    font-size: 15px;
    margin-bottom: 50px;
  }

  h6 {
    text-transform: uppercase;
    color: $silver-chalice;
    font-weight: bold;
    margin-bottom: 25px;
  }

  h1 {
    text-transform: capitalize;
    font-weight: bold;
    color: $lima;
    margin-bottom: 60px;
  }

  #testimonial-award-section {
    margin-top: 25px;
  }
}
</style>