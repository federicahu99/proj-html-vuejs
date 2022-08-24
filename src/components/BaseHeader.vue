<template>
  <div>
    <div id="upper-header">
      <div class="container">
        <div class="d-flex row justify-content-between">
          <div class="col">
            <i class="fa-solid fa-phone"></i>
            Call us for a Free Quote: 1.800.555.6789
          </div>
          <div>
            <BaseSocial class="col justify-content-between" />
          </div>
        </div>
      </div>
    </div>
    <!-- end of upper header, starts here the down side -->
    <div id="down-side">
      <div class="container">
        <div class="d-flex row">
          <figure class="col">
            <BaseLogo />
          </figure>
          <ul
            class="col d-flex justify-content-end align-items-center"
            id="menu-bar"
          >
            <!-- responsive menu header -->
            <i class="fa-solid fa-bars d-md-none"></i>
            <li
              v-for="(menu, i) in menuHeader"
              :key="i"
              class="d-none d-md-block"
            >
              <a href="menu.url">{{ menu.link }}</a>
            </li>
            <div>
              <BaseButton text="FREE QUOTE" class="d-none d-lg-block" id="header-button"/>
            </div>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BaseSocial from "./BaseSocial.vue";
import BaseLogo from "./BaseLogo.vue";
import BaseButton from "./BaseButton.vue";

export default {
  name: "BaseHeader",
  components: {
    BaseSocial,
    BaseLogo,
    BaseButton,
  },
  props: {
    menuHeader: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#upper-header {
  height: 70px;
  background-color: $lima;
  color: $mercury;
  font-size: 13px;
  padding-top: 10px;
  line-height: 300%;
}

// down side of header (option menu)

#down-side {
  background-color: none;
  padding: 10px;

  #menu-bar {
    font-size: 25px;
    color: $lima;
    transition: 0.4s;
    margin-left: -10px;

    li {
      margin-right: 20px;
      color: $shark;
      font-weight: bold;
      margin-top: 15px;
      font-size: 13px;
      transition: 0.4s;
      // effects on header options
      &:hover,
      &:active {
        border-bottom: 2px solid $lima;
        color: $lima;
        scale: 110%;
      }
    }

    a {
      color: $shark;

    }
    figure {
      width: 140px;
      margin-top: 10px;
    }
  }
  #header-button{
    padding-top: 5px;
    font-weight: bolder;
  }
}
</style>