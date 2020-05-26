<script>
  import MobileMenu from "./MobileMenu.svelte";
</script>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 12px 0;
    background-color: #fff;
    border-bottom: 1px solid hsl(0, 0%, 66.7%);
    z-index: 1;
  }

  .logo-wrapper img {
    height: auto;
    width: 170px;
    border: 0;
    vertical-align: middle;
  }

  .links-wrapper ul {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    flex-wrap: wrap;
    padding: 0;
  }

  .links-wrapper li {
    list-style: none;
  }

  .links-wrapper li a {
    color: #2275f4;
    font-weight: 500;
  }

  .links-wrapper li a:hover {
    color: #75a8f6;
  }

  .logo-wrapper {
    display: flex;
    align-items: center;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .action-item a {
    padding: 10px 23px;
    box-shadow: 0 2px 7px hsla(0, 0%, 0%, 0.5);
    background-color: #fff;
    margin-left: 20px;
  }

  @media screen and (min-width: 992px) {
    .container-fluid {
      padding-right: 56px;
      padding-left: 56px;
    }

    li a {
      font-size: 14px;
      padding: 8px 11px;
    }
  }

  @media screen and (min-width: 768px) and (max-width: 992px) {
    .container-fluid {
      padding-right: 45px;
      padding-left: 45px;
    }

    li a {
      font-size: 12px;
      padding: 8px 5px;
    }
  }

  @media screen and (max-width: 768px) {
    .container-fluid {
      padding-right: 10px;
      padding-left: 10px;
    }

    .action-item a {
      font-size: 12px;
      padding: 5px 18px;
      margin-left: 0;
    }

    header {
      padding: 0;
    }

    .logo-wrapper img {
      width: 110px;
      height: auto;
    }

    .logo-wrapper a {
      margin-left: 20px;
    }

    nav li:not(.action-item) {
      display: none;
    }
  }
</style>

<header>
  <div class="container-fluid">
    <div class="row">
      <div class="logo-wrapper col-6 col-sm-6 col-md-3">
        <a href="/">
          <img src="header-logo.png" alt="Skygear Auth Logo" />
        </a>
      </div>
      <div class="links-wrapper col-6 col-sm-6 col-md-9">
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
              <a href="/pricing">Pricing</a>
            </li>
            <li>
              <a>Open Sources</a>
            </li>
            <li class="action-item">
              <a>Talk to Us</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</header>
<MobileMenu />
