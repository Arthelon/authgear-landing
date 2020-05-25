<style>
  .trusted {
    background-color: #e7e7e7;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .trusted__title-wrapper {
    display: flex;
    align-items: center;
  }

  .trusted__title {
    margin: 0;
    font-size: 18px;
    font-weight: bold;
    color: #393939;
  }

  .trusted__img-wrapper {
    display: flex;
    align-items: center;
    height: 100%;
    max-width: 200px;
  }

  .trusted__img {
    max-width: 100%;
    max-height: 100px;
  }

  @media screen and (min-width: 768px) {
    .trusted {
      padding-top: 80px;
      padding-bottom: 85px;
    }

    .trusted__title-wrapper {
      flex: 0 0 20%;
      max-width: 20%;
    }

    .container-fluid {
      padding-left: 56px;
      padding-right: 56px;
    }
  }

  @media screen and (max-width: 768px) {
    .trusted {
      padding-top: 25px;
      padding-bottom: 80px;
    }

    .trusted__title-wrapper {
      justify-content: center;
    }

    .trusted__img-wrapper {
      padding-top: 67px;
      margin: 0 auto;
      justify-content: center;
    }
  }
</style>

<section class="trusted">
  <div class="container-fluid">
    <div class="row">
      <div class="trusted__title-wrapper col-12">
        <h3 class="trusted__title">Trusted by</h3>
      </div>
      <div class="col-12 col-md-3">
        <div class="trusted__img-wrapper">
          <img
            class="trusted__img"
            src="trusted/hkpc-logo.png"
            alt="HKPC Logo" />
        </div>
      </div>
      <div class="col-12 col-md-3">
        <div class="trusted__img-wrapper">
          <img
            class="trusted__img"
            src="trusted/cmic-logo.png"
            alt="CMIC Logo" />
        </div>
      </div>
      <div class="col-12 col-md-3">
        <div class="trusted__img-wrapper">
          <img
            class="trusted__img"
            src="trusted/rees-logo.png"
            alt="REES Logo" />
        </div>
      </div>
    </div>
  </div>
</section>
