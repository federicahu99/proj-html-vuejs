<template>
  <div id="footer-bg">
    <div id="footer-smaller-bg">

    </div>
  </div>
</template>

<script>
export default {
    name: "BaseFooter"
}
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#footer-bg {
    background-color: $lima;
    height: 600px;
    position: relative;

    #footer-smaller-bg{
        height: 500px;
        width: 100%;
        background-color: $white;
        position: absolute;
        bottom: 75px;
        left: 0;
    }
}


</style>