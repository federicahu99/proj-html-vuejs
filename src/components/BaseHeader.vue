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
        <ul class="col d-flex justify-content-end align-items-center" id="menu-bar">
          <i class="fa-solid fa-bars d-sm-none"></i>
          <li v-for="(menu, i) in menuHeader" :key="i" class="d-none d-sm-block">
            <a href="menu.url">{{menu.link}}</a>
          </li>
        </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BaseSocial from "./BaseSocial.vue";
import BaseLogo from "./BaseLogo.vue";

export default {
  name: "BaseHeader",
  components: {
    BaseSocial,
    BaseLogo,
  },
  props: {
    menuHeader: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#upper-header {
  height: 45px;
  background-color: $lima;
  color: $mercury;
  font-size: 13px;
  padding-top: 10px;
}

 #down-side {
   background-color: none;

   #menu-bar {
    font-size: 25px;
    color: $lima;
    transition: 0.4s;
    margin-left: -10px;

    &:hover,
    &:active{
      scale:103%;
    }
   }

   li {
     margin-right: 20px;
     color: $shark;
     font-weight: bold;
     margin-top: 15px;
     font-size: 13px;
   }
   a {
     color: $shark;
     &:hover,
     &:active {
       border-bottom: 2px solid $lima;
       color: $lima;
     }
   }
   figure {
     width: 140px;
     margin-top: 10px;
   }
 }
</style>