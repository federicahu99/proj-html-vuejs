<template>
  <div class="d-flex justify-content-between" id="social">
    <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
    <a href="#"><i class="fa-brands fa-twitter"></i></a>
    <a href="#"><i class="fa-brands fa-instagram"></i></a>
    <a href="#"><i class="fa-brands fa-youtube"></i></a>
  </div>
</template>

<script>

export default {
  name: "BaseSocial",
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";
#social {
  width: 130px;
  font-size: 16px;

  a {
    color: $white;
    margin: 0 5px;

    &:hover{
      color: $denim;
    }
  }
}
</style>