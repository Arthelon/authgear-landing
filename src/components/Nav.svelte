<script>

</script>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 12px 0;
    background-color: #fff;
    border-bottom: 1px solid hsla(0, 0%, 86%, 0.4);
    z-index: 999;
  }

  img {
    height: 38px;
    width: 170px;
  }

  ul {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    flex-wrap: wrap;
    padding: 0;
  }

  li {
    list-style: none;
  }

  li a {
    color: var(--primary);
    cursor: pointer;
    font-weight: 500;
  }

  li a:hover {
    color: #75a8f6;
  }

  .logo-wrapper {
    display: flex;
    align-items: center;
  }

  .logo-wrapper a {
    cursor: pointer;
  }
  .container-fluid {
    max-width: var(--content-max-width);
  }

  .action-link {
    padding: 10px 23px;
    box-shadow: 0 2px 7px hsla(0, 0%, 0%, 0.5);
    background-color: #fff;
    margin-left: 20px;
  }

  @media screen and (min-width: 40em) {
    .container-fluid {
      padding-right: 3.5rem;
      padding-left: 3.5rem;
    }

    li a {
      font-size: 14px;
      padding: 0.5rem 0.7rem;
    }
  }

  @media screen and (min-width: 40em) and (max-width: 64em) {
    .container-fluid {
      padding-right: 2.8rem;
      padding-left: 2.8rem;
    }

    li a {
      font-size: 11px;
      padding: 0.5rem 0.3rem;
    }
  }
</style>

<header>
  <div class="container-fluid">
    <div class="row">
      <div class="logo-wrapper col-sm-6 col-md-3">
        <a href="/">
          <img src="header-logo.png" alt="Skygear Auth Logo" />
        </a>
      </div>
      <div class="col-sm-6 col-md-9">
        <nav>
          <ul>
            <li>
              <a>Features</a>
            </li>
            <li>
              <a>Comparison</a>
            </li>
            <li>
              <a>Documentation</a>
            </li>
            <li>
              <a>Pricing</a>
            </li>
            <li>
              <a>Open Source</a>
            </li>
            <li>
              <a class="action-link">Talk to Us</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</header>
