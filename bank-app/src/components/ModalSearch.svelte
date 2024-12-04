<script>
  import SearchBar from "./SearchBar.svelte";

  export var showModalSearch = false;

  const turnOff = () => {
    showModalSearch = false;
  };

  const handleClickSearch = () => {};
</script>

<div class="modal-search {showModalSearch ? 'show' : ''}">
  <div class="search-container">
    <div class="modal-head">
      <h5>Search</h5>
      <button on:click={turnOff}><i class="bi bi-x"></i></button>
    </div>
    <div class="modal-content">
      <div class="search">
        <SearchBar
          handleClick={handleClickSearch}
          placeholder="Search here,..."
          width="100%"
          m_top="0"
          m_bot="1em"
        ></SearchBar>
      </div>
      <div class="title">Recent searches</div>
      <div class="recent-list">
        <a href="/" class="recent-item">Credit cards</a>
        <a href="/" class="recent-item">Saving</a>
      </div>
      <div class="title">Combo products that fits your life stage</div>
      <div class="promo-list">
        <div class="promo-item">
          <a href="/" class="promo-item-link">
            <div class="logo">
              <img
                src="https://www.vietcombank.com.vn/-/media/Project/VCB-Sites/VCB/Home-page/KHCN/Popup/phat-trien-su-nghiep.svg?h=32&w=32&ts=00010101000000&hash=2B2E1B282DDDA74A6CF1BF906795F923"
                alt=""
              />
            </div>
            <div class="content">
              <div class="strong"><strong>Career development</strong></div>
              <div class="p">
                <strong>E-banking, Savings, Investments</strong>
              </div>
            </div>
          </a>
        </div>
        <div class="promo-item">
          <a href="/" class="promo-item-link">
            <div class="logo">
              <img
                src="https://www.vietcombank.com.vn/-/media/Project/VCB-Sites/VCB/Home-page/KHCN/Popup/Xay-dung-to-am.svg?h=32&w=32&ts=00010101000000&hash=69556AA33EB131B676484A5FB5F28336"
                alt=""
              />
            </div>
            <div class="content">
              <div class="strong"><strong>Path to parenthood</strong></div>
              <div class="p">
                <strong>Loans, Insurances, Cards</strong>
              </div>
            </div>
          </a>
        </div>
        <div class="promo-item">
          <a href="/" class="promo-item-link">
            <div class="logo">
              <img
                src="https://www.vietcombank.com.vn/-/media/Project/VCB-Sites/VCB/Home-page/KHCN/Popup/phat-trien-su-nghiep.svg?h=32&w=32&ts=00010101000000&hash=2B2E1B282DDDA74A6CF1BF906795F923"
                alt=""
              />
            </div>
            <div class="content">
              <div class="strong"><strong>Retirement plans</strong></div>
              <div class="p">
                <strong>Savings, Money Transfer Services, Insurances</strong>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .modal-search {
    z-index: 10;
    position: fixed;
    display: none;
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    top: 0;
  }

  .modal-search .search-container {
    z-index: 1050;
    height: 87%;
    width: 45%;
    background-color: #fff;
    margin: auto;
    flex-direction: column;
    align-items: center;
    border-radius: 24px;
    border: none;
    top: 40%;
    left: 50%;
  }

  .modal-search.show {
    display: flex;
  }

  .modal-search .search-container .modal-head {
    position: relative;
    align-items: center;
    justify-content: center;
    display: flex;
    text-align: center;
    padding: 5px;
    border-bottom: 1px solid #ddd;
    font-family: Manrope, sans-serif;
    font-style: normal;
    font-weight: 700;
    font-size: 1.25rem;
    line-height: 1.875rem;
  }

  .modal-search .search-container .modal-head h5{
    font-size: 1.25rem !important;
    margin-top: .5rem;
  }

  .modal-search .search-container button {
    position: absolute;
    background-color: transparent;
    border: none;
    cursor: pointer;
    color: #000;
    font-size: 2em;
    top: 10%;
    right: 2%;
  }

  .modal-search .search-container .modal-content {
    padding: 20px;
  }

  .modal-search .search-container .modal-content .title {
    height: 24px;
    font-family: Manrope, sans-serif;
    font-style: normal;
    font-weight: 700;
    font-size: 1.125rem;
    line-height: 1.5rem;
    color: rgba(0, 0, 0, 0.8);
    margin-bottom: 0.75rem;
  }

  .modal-search .search-container .modal-content .recent-list {
    display: flex;
    flex-wrap: wrap;
    padding: 0;
    margin-bottom: 2rem;
  }

  .modal-search .search-container .modal-content .recent-item {
    padding: 0.25rem 0.75rem;
    min-height: 32px;
    background: rgba(0, 0, 0, 0.05);
    border-radius: 100px;
    color: rgba(0, 0, 0, 0.8);
    font-family: Manrope, sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 1rem;
    line-height: 1.5rem;
    letter-spacing: -0.02em;
    cursor: pointer;
    white-space: nowrap;
    overflow: hidden;
    position: relative;
    font-weight: 700;
  }

  .modal-search .search-container .modal-content .recent-item:not(:last-child) {
    margin-right: 0.5rem;
  }

  .modal-search .search-container .modal-content .recent-item:hover {
    background: linear-gradient(343deg, #a8d08d 0%, #f3ffe9 100%);
  }

  a {
    text-decoration: none !important;
  }

  .modal-search .search-container .modal-content .promo-list {
    margin: 0;
    width: 100%;
    padding: 0;
  }

  .modal-search .search-container .modal-content .promo-item {
    background-color: #f6f6f6;
    border-radius: 1rem;
    height: 100%;
    padding: .75em;
  }

  .modal-search .search-container .modal-content .promo-item:not(:last-child) {
    margin-bottom: 1rem;
  }

  .modal-search .search-container .modal-content .promo-item .promo-item-link {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .modal-search
    .search-container
    .modal-content
    .promo-item
    .promo-item-link
    .logo {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 1rem;
  }

  .modal-search
    .search-container
    .modal-content
    .promo-item
    .promo-item-link
    .logo img{
    width: 48px;
    height: 48px;
  }

  .modal-search
    .search-container
    .modal-content
    .promo-item
    .promo-item-link
    .content {
    width: 100%;
  }

  .modal-search
    .search-container
    .modal-content
    .promo-item
    .promo-item-link
    .content
    .strong {
    font-family: Manrope, sans-serif;
    font-style: normal;
    font-weight: 700;
    font-size: 1.25rem;
    line-height: 1.875rem;
    color: rgba(0, 0, 0, 0.8);
  }

  .modal-search
    .search-container
    .modal-content
    .promo-item
    .promo-item-link
    .content
    .p {
    font-family: Manrope, sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 1rem;
    line-height: 1.5rem;
    letter-spacing: -0.02em;
    display: flex;
    color: rgba(0, 0, 0, 0.6);
  }
</style>
