<template>
  <div id="jumbotron"> 
    <div id="jumbotron-upper">
      <div class="container" id="jumbotron-text">
        <h6>moving without the hassle</h6>
        <h1>we make it simple</h1>
        <h6>professional service with quality and custumer satisfaction</h6>
      </div>
    </div>
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
  height: 500px;
  background-image: url(../assets/images/avada-movers-homeherobackground-final.jpg);
  background-position: center;
  background-size: 130%;

  #jumbotron-text {
    width: 550px;
    height: 500px;
    text-align: center;
    padding: 203px 10px;

    h1 {
      text-transform: uppercase;
      font-weight: bold;
      color: $shark;
      margin: 18px;
    }

    h6 {
      text-transform: uppercase;
      font-size: 12px;
      font-weight: bold;
      color: $dove-grey;
    }
  }
}

//Blue jumbotron section

#jumbotron-under {
  height: 120px;
  background-color: $denim;
  margin: 0 auto;

  #jumbotron-link {
    width: 300px;
    padding: 45px 0;
    text-transform: uppercase;

    a {
      color: $mercury;
    }
  }
}
</style>