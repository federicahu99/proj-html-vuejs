<template>
  <div id="header">
    <div id="upper-side" class="d-flex justify-content-between  align-items-center" >
      <div>
        <i class="fa-solid fa-phone"></i
        ><span> Call us for a Free Quote: 1.800.5555.6789</span>
      </div>
      <div>
        <BaseSocial />
      </div>
    </div>
  </div>
</template>

<script>
import BaseSocial from "./BaseSocial.vue";

export default {
  name: "BaseHeader",
  components: {
    BaseSocial,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#upper-side {
  height: 30px;
  background-color: $lima;
  color: white;
  font-size: 12px;
}
</style>