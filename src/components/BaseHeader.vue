<template>
  <div id="header">
    <div id="upper-side">
      <!-- upper header for social and number phone -->
      <div class="container d-flex justify-content-between align-items-center">
        <div>
          <i class="fa-solid fa-phone"></i
          ><span> Call us for a Free Quote: 1.800.5555.6789</span>
        </div>
        <div>
          <BaseSocial />
        </div>
      </div>
    </div>

    <!-- logo menu btn of header -->
    <div
      id="under-side"
      class="container d-flex justify-content-between align-items-center"
    >
      <figure>
        <a href="#">
          <img
            src="../assets/images/avada-movers-logo.png"
            alt="Avada Movers logo"
          />
        </a>
      </figure>
      <div
        id="menu-logo"
        class="d-flex justify-content-between align-items-center"
      >
        <ul class="d-flex justify-content-between align-items-center">
          <li v-for="(menu, i) in menuHeader" :key="i">
            <a href="menu.link"> {{ menu.name }}</a>
          </li>
        </ul>
        <BaseButton text="Free Quote" />
      </div>
    </div>
  </div>
</template>

<script>
import BaseSocial from "./BaseSocial.vue";
import BaseButton from "./BaseButton.vue";

export default {
  name: "BaseHeader",
  components: {
    BaseSocial,
    BaseButton,
  },
  props: {
    menuHeader: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#header {
  position: relative;

  #upper-side {
    height: 40px;
    background-color: $lima;
    color: $mercury;
    font-size: 12px;
    padding-top: 10px;
  }

  #under-side {
    position: absolute;
    left: 230px;
    top: 40px;

    li {
      margin-right: 30px;
      color: $shark;
      font-weight: bold;
      margin-top: 15px;
    }

    figure {
      width: 140px;
      margin-top: 10px;

      img {
        width: 100%;
      }
    }
  }
}
</style>