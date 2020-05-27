<script>
  import MobileMenu from "./MobileMenu.svelte";
</script>

<style>
  .nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 12px 0;
    background-color: #fff;
    border-bottom: 1px solid hsl(0, 0%, 66.7%);
    z-index: 1;
  }

  .nav__logo-wrapper {
    display: flex;
    align-items: center;
  }

  .nav__logo-img {
    height: auto;
    width: 170px;
    border: 0;
    vertical-align: middle;
  }

  .nav__links-list {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    flex-wrap: wrap;
    padding: 0;
  }

  .nav__link-item {
    list-style: none;
  }

  .nav__link {
    color: #2275f4;
    font-weight: 500;
  }

  .nav__link:hover {
    color: #75a8f6;
  }

  .container-fluid {
    max-width: 1200px;
  }

  .nav__link--action {
    box-shadow: 0 2px 7px hsla(0, 0%, 0%, 0.5);
    background-color: #fff;
    margin-left: 20px;
  }

  @media screen and (min-width: 992px) {
    .container-fluid {
      padding-right: 56px;
      padding-left: 56px;
    }

    .nav__link {
      font-size: 14px;
      padding: 8px 11px;
    }

    .nav__link--action {
      padding: 10px 23px;
    }
  }

  @media screen and (min-width: 768px) and (max-width: 992px) {
    .container-fluid {
      padding-right: 45px;
      padding-left: 45px;
    }

    .nav__link {
      font-size: 12px;
      padding: 8px 5px;
    }

    .nav__link--action {
      padding: 10px 23px;
    }
  }

  @media screen and (max-width: 768px) {
    .container-fluid {
      padding-right: 10px;
      padding-left: 10px;
    }

    .nav__link--action {
      font-size: 12px;
      padding: 5px 18px;
      margin-left: 0;
    }

    .nav {
      padding: 0;
    }

    .nav__logo-img {
      width: 110px;
      height: auto;
    }

    .nav__logo-img {
      margin-left: 20px;
    }

    .nav__link:not(.nav__link--action) {
      display: none;
    }
  }
</style>

<header class="nav">
  <div class="container-fluid">
    <div class="row">
      <div class="nav__logo-wrapper col-6 col-sm-6 col-md-3">
        <a href="">
          <img
            class="nav__logo-img"
            src="img/header-logo.png"
            alt="Skygear Auth Logo" />
        </a>
      </div>
      <div class="col-6 col-sm-6 col-md-9">
        <nav>
          <ul class="nav__links-list">
            <li class="nav__link-item">
              <a class="nav__link">Features</a>
            </li>
            <li class="nav__link-item">
              <a class="nav__link">Comparison</a>
            </li>
            <li class="nav__link-item">
              <a class="nav__link">Documentation</a>
            </li>
            <li class="nav__link-item">
              <a class="nav__link" href="pricing">Pricing</a>
            </li>
            <li class="nav__link-item">
              <a class="nav__link">Open Sources</a>
            </li>
            <li class="nav__link-item">
              <a class="nav__link nav__link--action">Talk to Us</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</header>
<MobileMenu />
