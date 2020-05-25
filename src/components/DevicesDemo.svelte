<style>
  .devices-demo {
    width: 100%;
    background-color: #d8d8d8;
  }

  .devices-demo__img-wrapper {
    position: relative;
    max-width: 870px;
  }

  .devices-demo__img {
    width: 100%;
  }

  @media screen and (min-width: 768px) {
    .devices-demo {
      padding-top: 30px;
    }

    .devices-demo__img-wrapper {
      padding-left: 56px;
      padding-right: 56px;
      bottom: -35px;
    }
  }

  @media screen and (max-width: 768px) {
    .devices-demo__img-wrapper {
      padding-left: 43px;
      padding-right: 65px;
      bottom: -18px;
    }
  }
</style>

<section class="devices-demo">
  <div class="container-fluid devices-demo__img-wrapper">
    <img
      class="devices-demo__img"
      src="devices-demo.png"
      alt="Demo of Skygear Auth on Mobile and Desktop devices" />
  </div>
</section>
