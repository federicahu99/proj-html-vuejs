<template>
  <div id="slogan-section" >
    <div class="row container">
      <div id="slogan-content" >
        <div class="col">
          <h6 class="d-none d-md-block">we remove the headache from moving</h6>
          <h1>move with ease</h1>
          <div id="line"></div>
          <div id="slogan-text" class="d-none d-md-block">
            With our super simple service we can take you from getting a quote,
            right through to being in your new home with all of your belongings
            securely packed and safely delivered, even in the rooms of your
            choice.
          </div>
          <BaseButton
            text="get a free quote now"
            id="slogan-button"
            class="d-none d-sm-block"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BaseButton from "./BaseButton.vue";
export default {
  name: "SloganSection",
  components: {
    BaseButton,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#slogan-section {
  height: 680px;
  background-image: url(../assets/images/avada-movers-movewithease-background-new.jpg);
  background-size: cover;
  padding-top: 115px;

  #slogan-content {
    max-width: 40%;
    border: 12.5px solid $hippie-green;
    padding: 25px 5px;
    background-color: $lima;
    color: $white;
    text-align: center;
    margin: auto 10% auto auto;
  }

  h1 {
    text-transform: capitalize;
    font-weight: bold;
    color: $lima;
    margin-bottom: 15px;
    color: $white;
    font-size: 35px;
  }

  h6 {
    color: $white;
    font-size: 11px;
  }

  #line {
    width: 57%;
    border-top: 2.5px solid $mantis;
    margin: 20px auto;
  }

  #slogan-text {
    font-size: 12px;
    margin:  0 auto;
  }

  #slogan-button {
    margin-top: 20px;
    text-transform: uppercase;
  }
}
</style>