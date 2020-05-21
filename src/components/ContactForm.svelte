<script>
  function handleSubmit(e) {
    e.preventDefault();
  }
</script>

<style>
  .contact-wrapper {
    display: flex;
  }

  .contact-wrapper .email-input {
    outline: none;
    border: none;
    border-bottom: 1px solid #979797;
  }

  .contact-wrapper .submit-btn {
    color: #fff;
    cursor: pointer;
    padding: 10px 24px;
    background: #166ff7;
    max-width: 120px;
    outline: none;
    border: none;
    border-radius: 2px;
    box-shadow: 0 2px 7px hsla(0, 0%, 0%, 0.5);
  }

  .contact-wrapper .submit-btn:hover {
    color: #1468a0;
  }

  @media screen and (min-width: 768px) {
    .contact-wrapper .email-input {
      flex: 3 3;
      margin-right: 20px;
    }
  }

  @media screen and (max-width: 768px) {
    .contact-wrapper {
      flex-direction: column;
    }

    .contact-wrapper .submit-btn {
      margin-top: 13px;
      margin-bottom: 30px;
    }
  }
</style>

<form class="contact-wrapper" on:submit={handleSubmit}>
  <input class="email-input" type="email" placeholder="Your Email" />
  <button class="submit-btn" type="submit">Talk to Us</button>
</form>
