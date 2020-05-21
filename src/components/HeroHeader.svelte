<style>
  section {
    background-color: #fff;
    padding: 164px 0 144px 0;
    color: #000;
  }

  .container-fluid {
    max-width: 75rem;
  }

  img {
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

  .contact-wrapper {
    display: flex;
  }

  .contact-wrapper input {
    outline: none;
    border: none;
    border-bottom: 1px solid #979797;
    padding-bottom: 10px;
  }

  .contact-wrapper button {
    color: #fff;
    cursor: pointer;
    height: fit-content;
    width: fit-content;
    padding: 10px 24px;
    background: #166ff7;
    outline: none;
    border: none;
    border-radius: 2px;
    box-shadow: 0 2px 7px hsla(0, 0%, 0%, 0.5);
  }

  .contact-wrapper button:hover {
    color: #1468a0;
  }

  @media screen and (min-width: 768px) {
    .container-fluid {
      padding-right: 3.5rem;
      padding-left: 3.5rem;
    }

    .tagline h1 {
      margin-bottom: 16px;
      font-size: 42px;
    }

    .contact-wrapper input {
      flex: 3 3;
      margin-right: 20px;
    }
  }

  @media screen and (max-width: 768px) {
    .container-fluid {
      padding-right: 1.8rem;
      padding-left: 1.8rem;
    }

    .tagline h1 {
      margin-bottom: 7px;
      font-size: 28px;
    }

    .contact-wrapper {
      flex-direction: column;
    }

    .contact-wrapper button {
      margin-top: 13px;
      margin-bottom: 30px;
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
        <div class="contact-wrapper">
          <input type="email" placeholder="Your Email" />
          <button>Talk to Us</button>
        </div>
      </div>
      <div class="col-12 col-md-7">
        <img src="hero-header-img.png" alt="Hero Header" />
      </div>
    </div>
  </div>
</section>
