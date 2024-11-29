<script>
    export let placeholder;
    export let handleClick = () => {}
    export let width;
    export let m_top;
</script>

<div class="home-search mt-5 mt-lg-4" on:click={handleClick} style="width: {width}; margin-top: {m_top} !important;">
  <i class="bi bi-search"></i>
  <input
    type="email"
    readonly
    class="form-control"
    id="home-search"
    placeholder={placeholder}
  />
</div>

<style>
  .home-search {
    display: flex;
    align-items: center;
    gap: 1rem;
    background: #fff;
    padding: 1rem 1.5rem;
    border-radius: 10rem;
    cursor: pointer;
    border: 1px solid rgba(0, 0, 0, .2);
  }

  .home-search i {
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    color: #074c31;
  }

  .home-search .form-control {
    border: none !important;
    box-shadow: none;
    padding: 0;
  }

  .home-search .form-control {
    display: block;
    width: 100%;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
    transition:
      border-color 0.15s ease-in-out,
      box-shadow 0.15s ease-in-out;
    cursor: pointer;
  }
</style>
