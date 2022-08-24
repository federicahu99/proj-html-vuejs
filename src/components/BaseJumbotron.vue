<template>
  <div id="jumbotron">
    <!-- first part of jumbo -->
    <div id="jumbotron-upper">
      <div class="container" id="jumbotron-text">
        <h6>moving without the hassle</h6>
        <h1>we make it simple</h1>
        <h6>professional service with quality and custumer satisfaction</h6>
      </div>
    </div>
    <!-- second part of jumbo -->
    <div id="jumbotron-under">
      <div id="jumbotron-link" class="container">
        <a href="#">
          <i class="fa-regular fa-paper-plane"></i> get a free quote online now!
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BaseJumbotron",
};
</script>

<style scoped lang="scss">
@import "../assets/sass/style.scss";

#jumbotron-upper {
  margin-top: -88px;
  height: 450px;
  background-image: url(../assets/images/avada-movers-homeherobackground-final.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;

  #jumbotron-text {
    width: 80%;
    text-align: center;
    padding-top: 145px;

    h1 {
      text-transform: uppercase;
      font-weight: bold;
      color: $shark;
      margin: 18px 0 ;
    }
  }
}

//Blue jumbotron section

#jumbotron-under {
  height: 120px;
  background-color: $denim;
  margin: 0 auto;

  #jumbotron-link {
    text-align: center;
    width: 80%;
    padding: 45px 0;
    text-transform: uppercase;

    a {
      color: $mercury;

      &:hover{
        border-bottom: 2px solid $white
      }
    }
  }
}
</style>