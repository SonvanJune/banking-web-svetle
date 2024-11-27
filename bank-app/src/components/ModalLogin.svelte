<script>
  export let show = false;
</script>

<div class="modal {show ? 'show' : ''}">
  <div class="login-group">
    <a href="/" class="login-link"
      ><div>
        Mono-Digi Bank <div class="small-txt">Personal Banking</div>
      </div>
      <i class="bi bi-caret-right-fill"></i></a
    >
    <div class="login-line"></div>
    <a href="/" class="login-link"
      ><div>
        Mono-Digi Biz
        <div class="small-txt">SME Banking</div>
      </div>
      <i class="bi bi-caret-right-fill"></i></a
    >
    <div class="login-line"></div>
    <a href="/" class="login-link"
      ><div>
        Mono-iBanking
        <div class="small-txt">Institutional Banking</div>
      </div>
      <i class="bi bi-caret-right-fill"></i></a
    >
    <div class="login-line"></div>
    <a href="/" class="login-link"
      ><div>
        Mono-Cashup
        <div class="small-txt">Institutional Banking</div>
      </div>
      <i class="bi bi-caret-right-fill"></i></a
    >
  </div>
</div>

<style>
  .modal {
    display: none;
    position: absolute;
    top: 100%;
    width: 120%;
    left: -20%;
    height: max-content;
    background-color: rgba(0, 0, 0, 0.5);
    animation: slideUp 0.4s ease-in-out forwards;
  }

  @keyframes slideUp {
    0% {
      transform: translateY(40px);
      opacity: 0;
    }
    100% {
      transform: translateY(0);
      opacity: 1;
    }
  }

  .modal.show {
    display: block;
  }

  .modal .login-group {
    display: flex;
    flex-direction: column;
    background: #fff;
    border-radius: 8px;
    padding: 0px 5px;
    width: 100%;
    height: auto;
    align-items: center;
  }

  .modal .login-group .login-link {
    transition: all 0.3s ease-out 0s !important;
    padding: 0.1rem 0.5rem;
    margin-top: 0.2em;
    margin-bottom: 0.2rem;
    height: 100%;
    width: 100%;
    color: rgba(0, 0, 0, 0.8);
    font-family: Manrope, sans-serif;
    font-weight: bold;
    text-decoration: none;
    font-size: 0.9rem;
    line-height: 1.5rem;
    white-space: nowrap;
    display: flex;
    border-radius: 5px;
    position: relative;
    text-align: left;
  }

  .modal .login-group .login-link .small-txt{
    font-size: 0.8rem;
    color: rgba(0, 0, 0, 0.5);
    font-weight: normal;
    text-align: left;
    white-space: nowrap;
  }

  .modal .login-group .login-line {
    left: 0;
    border-top: 0.5px solid rgba(0, 0, 0, 0.1);
    width: 100%;
    height: 1px;
    display: block;
  }

  .modal .login-group .login-link:hover {
    background-color: rgb(236 251 210);
  }

  .modal .login-group .login-link:hover i {
    display: block;
  }

  .modal .login-group .login-link i {
    display: none;
    position: absolute;
    right: 5%;
    top: 25%;
  }
</style>
