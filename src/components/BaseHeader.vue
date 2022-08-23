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
    <div id="under-side" class="container d-flex justify-content-between align-items-center">
      <figure>
        <img
          src="../assets/images/avada-movers-logo.png"
          alt="Avada Movers logo"
        />
      </figure>
      <div id="menu-logo" class="d-flex justify-content-between align-items-center">
        <ul class="d-flex justify-content-between align-items-center">
            <li v-for="menu in menuHeader" :key="menu"><a href="#"> {{ menu }}</a></li>
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
    menuHeader: Array
  }
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#upper-side {
  height: 40px;
  background-color: $lima;
  color: white;
  font-size: 12px;
  padding-top: 10px;
}

#under-side {
    li {
        margin-right: 15px;
    }
}
</style>