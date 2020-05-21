<script>
  import ContactForm from "./ContactForm.svelte";
</script>

<style>
  section {
    background-color: #fff;
    padding: 164px 0 144px 0;
    color: #000;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .hero-img {
    max-width: 100%;
    height: auto;
  }

  .tagline h1 {
    font-weight: 900;
  }

  .tagline p {
    font-size: 18px;
    font-weight: 400;
    margin-bottom: 52px;
  }

  @media screen and (min-width: 768px) {
    .container-fluid {
      padding-right: 56px;
      padding-left: 56px;
    }

    .tagline h1 {
      margin-bottom: 16px;
      font-size: 42px;
    }
  }

  @media screen and (max-width: 768px) {
    .container-fluid {
      padding-right: 18px;
      padding-left: 18px;
    }

    .tagline h1 {
      margin-bottom: 7px;
      font-size: 28px;
    }
  }
</style>

<section>
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
      <div class="col-12 col-md-7">
        <img class="hero-img" src="hero-header-img.png" alt="Hero Header" />
      </div>
    </div>
  </div>
</section>
