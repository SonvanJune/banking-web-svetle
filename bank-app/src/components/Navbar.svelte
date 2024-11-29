<script>
  import ModalLogin from "./ModalLogin.svelte";

  let showModal = false;
</script>

<div class="navbar">
  <div class="container-fluid">
    <div class="row">
      <div class="col-md-2">
        <div class="logo"></div>
      </div>
      <div class="col-md-8">
        <div class="menu">
          <a class="item active" href="/"
            >Product&Service<i class="bi bi-caret-down-fill"></i>
            <div class="item-line"></div></a
          >
          <a class="item" href="/"
            >Tool&Utilities<i class="bi bi-caret-down-fill"></i>
            <div class="item-line"></div></a
          >
          <a class="item" href="/"
            >Contact&Support<i class="bi bi-caret-down-fill"></i>
            <div class="item-line"></div></a
          >
          <a class="item" href="/"
            >Safe transaction principles <div class="item-line"></div></a
          >
        </div>
      </div>
      <div class="col-md-2">
        <div class="login">
          <button
            on:mouseenter={() => (showModal = true)}
            on:mouseleave={() => (showModal = false)}
          >
            <i class="bi bi-box-arrow-in-right"></i>
            <span>Login</span>
            <ModalLogin show={showModal} />
          </button>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .navbar .logo {
    background-image: url("../../public/img/logo.png");
    background-size: cover;
    width: 60px;
    height: 60px;
  }

  .navbar .menu {
    display: flex;
    justify-content: left;
    flex-direction: row;
    height: 100%;
  }

  .navbar .menu .item {
    font-family: Manrope, sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 1rem;
    line-height: 1rem;
    letter-spacing: -0.02em;
    color: #fff;
    text-decoration: none;
    margin-right: 3rem;
    white-space: nowrap;
    height: 100%;
    position: relative;
    display: flex;
    align-items: center;
  }

  .navbar .menu .item .item-line {
    display: none;
    width: 100%;
    height: 4px;
    background-color: #85b94d;
    position: absolute;
    bottom: 0;
    border-radius: 2px;
  }

  .navbar .menu .item:hover .item-line {
    display: block;
  }

  .navbar .menu .item i {
    position: absolute;
    top: 40%;
    right: -20%;
  }

  .navbar .login {
    display: flex;
    justify-content: right;
    align-items: center;
    height: 100%;
    width: 110%;
  }

  .row {
    width: 100% !important;
  }

  .navbar .login button {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.75rem 1.5rem 0.75rem 1rem;
    z-index: 3;
    background-color: #a1c038;
    cursor: pointer;
    width: 155px;
    position: relative;
    order: 1;
    border: none;
    font-family: "Manrope SemiBold", sans-serif;
    font-style: normal;
    font-weight: 600;
    font-size: 1rem;
    line-height: 1.5rem;
    letter-spacing: -0.02em;
    border-radius: 8px;
    color: rgba(0, 0, 0, 0.8);
  }

  .navbar .login button:hover {
    background: linear-gradient(
        0deg,
        rgba(255, 255, 255, 0.2),
        rgba(255, 255, 255, 0.2)
      ),
      #a1c038;
  }

  .navbar .login button i {
    margin-right: 0.75rem;
    font-size: 1.4em;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
