<template>
  <div id="option-menu">
    <h4>{{ optionTitle }}</h4>
    <ul class="footer-option">
      <li class="footer-option" v-for="(option, i) in options" :key="i">
        <a :href="option.url"
          ><i class="fa-solid fa-angle-right"></i> {{ option.link }}</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "OptionMenuFooter",
  props: { options: Array, optionTitle: String },
};
</script>

<style scoped lang="scss" >
@import "../assets/sass/style.scss";

#option-menu {
  padding-top: 50px;

  h4 {
    font-size: 22px;
    font-weight: bold;
  }

  .footer-option {
    margin: 0;
    padding: 0;
    font-size: 14px;
    line-height: 180%;
  }

  a {
    color: $shark;
    transition: 0.4s;

    &:hover,
    &:active {
      font-size: 17px;
      font-weight: bold;
      color: $lima;
    }
  }
}
</style>