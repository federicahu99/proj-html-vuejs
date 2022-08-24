<template>
  <div>
    <a href="#" id="logo">
      <img
        src="./../assets/images/avada-movers-logo.png"
        alt="Avda logo image"
      />
    </a>
  </div>
</template>

<script>
export default {
  name: "BaseLogo",
};
</script>

<style scoped lang="scss">
#logo {
  display: block;

  img {
    width: 140px;
    transition: 0.5s;

    &:hover {
      scale: 110%;
    }
  }
}
</style>