<style>
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

  #mobile-menu {
    display: none;
    position: fixed;
    top: 26px;
    left: 10px;
    z-index: 2;
    cursor: pointer;

    -webkit-user-select: none;
    user-select: none;
  }

  #mobile-menu span {
    display: block;
    width: 25px;
    height: 4px;
    margin-bottom: 5px;
    position: relative;
    background: hsl(0, 0%, 66.7%);
    border-radius: 3px;
    z-index: 1;
    transform-origin: 4px 0px;
    transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1),
      background 0.5s cubic-bezier(0.77, 0.2, 0.05, 1), opacity 0.55s ease;
  }

  #mobile-menu input {
    display: block;
    width: 32px;
    height: 32px;
    position: absolute;
    top: -7px;
    left: -5px;

    cursor: pointer;

    opacity: 0;
    z-index: 2;
  }

  #mobile-menu span:first-child {
    transform-origin: 0% 0%;
  }

  #mobile-menu span:nth-last-child(2) {
    transform-origin: 0% 100%;
  }

  #mobile-menu input:checked ~ span {
    opacity: 1;
    transform: rotate(45deg) translate(1px, 1px);
    background: hsl(0, 0%, 66.7%);
  }

  #mobile-menu input:checked ~ span:nth-last-child(3) {
    opacity: 0;
    transform: rotate(0deg) scale(0.2, 0.2);
  }

  #mobile-menu input:checked ~ span:nth-last-child(2) {
    transform: rotate(-45deg) translate(3px, -1px);
  }

  #mobile-menu-list {
    position: absolute;
    width: 300px;
    margin: -100px 0 0 -50px;
    padding: 50px 15px 50px 80px;
    padding-top: 125px;
    background: hsla(0, 0%, 100%, 0.95);
    list-style-type: none;
    -webkit-font-smoothing: antialiased;
    border-right: 1px solid #e8e8e8;
    min-height: calc(100vh + 100px);
    transform-origin: 0 0;
    transform: translate(-100%);
    transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }

  #mobile-menu-list li {
    width: 100%;
    padding: 10px 0;
    font-size: 16px;
  }

  #mobile-menu input:checked ~ ul {
    transform: none;
  }
  @media screen and (max-width: 768px) {
    #mobile-menu {
      display: block;
    }
  }
</style>

<div id="mobile-menu">
  <input type="checkbox" />
  <span />
  <span />
  <span />
  <ul id="mobile-menu-list">
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
  </ul>
</div>
