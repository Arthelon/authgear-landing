<script>
  import ContactForm from "./ContactForm.svelte";
</script>

<style>
  .hero-section {
    background-color: #fff;
    color: #000;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .hero-img {
    max-width: 100%;
  }

  .hero-img-wrapper {
    display: flex;
    justify-content: flex-end;
  }

  .tagline h1 {
    font-weight: 900;
    line-height: 1.4;
  }

  .tagline p {
    margin-top: 0;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.5;
  }

  @media screen and (min-width: 768px) {
    .hero-section {
      padding: 164px 0 144px 0;
    }

    .hero-img {
      max-height: 305px;
    }

    .container-fluid {
      padding-right: 56px;
      padding-left: 56px;
    }

    .tagline h1 {
      margin-bottom: 16px;
      font-size: 42px;
    }

    .tagline p {
      margin-bottom: 52px;
    }
  }

  @media screen and (max-width: 768px) {
    .hero-section {
      padding: 85px 0 40px 0;
    }

    .hero-img {
      height: auto;
    }

    .container-fluid {
      padding-right: 18px;
      padding-left: 18px;
    }

    .tagline h1 {
      margin-bottom: 7px;
      font-size: 28px;
    }

    .tagline p {
      margin-bottom: 30px;
    }
  }
</style>

<section class="hero-section">
  <div class="container-fluid">
    <div class="row">
      <div class="col-12 col-md-5 t tagline">
        <h1>Don't Compromise Security, Let us help</h1>
        <p>
          Rapidly integrate authentication for your web and mobile applications,
          with security and reliability
        </p>
        <ContactForm />
      </div>
      <div class="hero-img-wrapper col-12 col-md-7">
        <img
          class="hero-img"
          src="/img/hero-header-img.png"
          alt="Hero Header" />
      </div>
    </div>
  </div>
</section>
