<style>
  .trustedby {
    background-color: #e7e7e7;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .trustedby__title-wrapper {
    display: flex;
    align-items: center;
  }

  .trustedby__title {
    margin: 0;
    font-size: 18px;
    font-weight: bold;
    color: #393939;
  }

  .trustedby__img-wrapper {
    display: flex;
    align-items: center;
    height: 100%;
    max-width: 200px;
  }

  .trustedby__img {
    max-width: 100%;
    max-height: 100px;
  }

  @media screen and (min-width: 768px) {
    .trustedby {
      padding-top: 80px;
      padding-bottom: 85px;
    }

    .trustedby__title-wrapper {
      flex: 0 0 20%;
      max-width: 20%;
    }

    .container-fluid {
      padding-left: 56px;
      padding-right: 56px;
    }
  }

  @media screen and (max-width: 768px) {
    .trustedby {
      padding-top: 25px;
      padding-bottom: 80px;
    }

    .container-fluid {
      padding-right: 18px;
      padding-left: 18px;
    }

    .trustedby__title-wrapper {
      justify-content: center;
    }

    .trustedby__img-wrapper {
      padding-top: 67px;
      margin: 0 auto;
      justify-content: center;
    }
  }
</style>

<section class="trustedby">
  <div class="container-fluid">
    <div class="row">
      <div class="trustedby__title-wrapper col-12">
        <h3 class="trustedby__title">Trusted by</h3>
      </div>
      <div class="col-12 col-md-3">
        <div class="trustedby__img-wrapper">
          <img
            class="trustedby__img"
            src="trustedby/hkpc-logo.png"
            alt="HKPC Logo" />
        </div>
      </div>
      <div class="col-12 col-md-3">
        <div class="trustedby__img-wrapper">
          <img
            class="trustedby__img"
            src="trustedby/cmic-logo.png"
            alt="CMIC Logo" />
        </div>
      </div>
      <div class="col-12 col-md-3">
        <div class="trustedby__img-wrapper">
          <img
            class="trustedby__img"
            src="trustedby/rees-logo.png"
            alt="REES Logo" />
        </div>
      </div>
    </div>
  </div>
</section>
