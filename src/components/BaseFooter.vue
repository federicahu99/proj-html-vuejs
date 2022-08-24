<template>
  <div id="footer-bg">
    <!-- Upper part of footer (white background section) -->

    <div id="footer-smaller-bg">
      <div class="container">
        <div class="row">
          <div class="col">
            <div>
              <h4>about</h4>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ad
                magnam ut quibusdam a blanditiis ullam, tempora laboriosam
                sapiente itaque.
              </p>
              <BaseLogo />
            </div>
          </div>
          <!-- First option menu -->
          <div class="col">
            <OptionMenuFooter
              optionTitle="Avada Movers"
              :options="menuFooterLeft"
            />
          </div>
          <!-- Second option menu -->
          <div class="col">
            <OptionMenuFooter
              optionTitle="Recent Post"
              :options="menuFooterRight"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- last part of footer (lime background section) -->
    <div class="container">
      <ul id="bottom-menu">
        <li v-for="(menu, i) in menuFooterBottom" :key="i">
          <a :href="menu.url"> {{ menu.link }} </a>
        </li>
      </ul>
      <div id="social-footer">
      <BaseSocial />
      </div>
    </div>
  </div>
</template>

<script>
import BaseLogo from "./BaseLogo.vue";
import OptionMenuFooter from "./OptionMenuFooter.vue";
import BaseSocial from "./BaseSocial.vue";

export default {
  name: "BaseFooter",
  components: { BaseSocial, OptionMenuFooter, BaseLogo },
  props: {
    menuFooterRight: Array,
    menuFooterLeft: Array,
    menuFooterBottom: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#footer-bg {
  background-color: $lima;
  height: 470px;
  position: relative;

  #footer-smaller-bg {
    height: 370px;
    width: 100%;
    background-color: $white;
    position: absolute;
    bottom: 75px;
    left: 0;

    h4 {
      text-transform: uppercase;
      font-weight: bold;
      margin: 30px 0;
    }

    p {
      font-size: 12px;
      margin-bottom: 35px;
      width: 90%;
    }
  }

  #bottom-menu {
    font-size: 10px;
    display: flex;
    justify-content: space-evenly;
    padding-top: 401px;

    a {
    color: $white;

    &:hover,
    &:active{
        color: $denim;
    }

    #social-footer {
        width: 110px;
    }
  }
}
}
</style>