<script>
  import ContactForm from "./ContactForm.svelte";
</script>

<style>
  .cta {
    background-color: #fff;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .cta__title {
    font-weight: 900;
    font-size: 42px;
    color: #393939;
    margin-top: 0;
    line-height: 1.4;
  }

  @media screen and (min-width: 768px) {
    .cta {
      padding-top: 80px;
      padding-bottom: 115px;
    }

    .container-fluid {
      padding-left: 56px;
      padding-right: 56px;
    }

    .cta__title {
      margin-bottom: 40px;
    }
  }

  @media screen and (max-width: 767px) {
    .cta {
      padding-top: 30px;
      padding-bottom: 25px;
    }

    .container-fluid {
      padding-right: 18px;
      padding-left: 18px;
    }

    .cta__title {
      margin-bottom: 20px;
    }
  }
</style>

<section class="cta">
  <div class="container-fluid">
    <div class="row">
      <div class="col-12">
        <h1 class="cta__title">Try Skygear Auth. Its awesome.</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-12 col-md-5">
        <ContactForm />
      </div>
    </div>
  </div>
</section>
