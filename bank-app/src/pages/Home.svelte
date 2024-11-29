<script>
  import ModalSearch from "../components/ModalSearch.svelte";
  import SearchBar from "../components/SearchBar.svelte";
  let showModal = false;

  const handleClickSearch = () => {
    showModal = !showModal;
  };
</script>

<main>
  <div class="container-fluid">
    <div class="row home">
      <div class="col-md-6 left-main">
        <div class="greeting">
          <img
            src="https://www.vietcombank.com.vn/-/media/Default-Website/Default-Images/Home-page/Icon-Thoi-Tiet/im_80_morning.svg?h=1114&w=1980&ts=00010101000000&hash=844E568D04E62EB3895057232E502A76"
            alt=""
          />
          <div class="greeting-text">
            <h2>Good Morning</h2>
            <p>What are you looking for</p>
          </div>
        </div>

        <SearchBar handleClick={handleClickSearch} placeholder="Credits cards, consumer loans,..." width=80% m_top=1em></SearchBar>
      </div>
      <div class="col-md-6"></div>
    </div>
  </div>
</main>
<ModalSearch showModalSearch={showModal} />

<style>
  .home {
    padding: 100px 0;
    position: relative;
  }

  .greeting {
    font-size: 2.5rem;
    width: 100%;
    position: relative;
    display: flex;
    flex-direction: row;
    align-items: center;
    color: #fff;
  }

  .greeting img {
    width: 80px;
    height: 80px;
  }

  .greeting .greeting-text {
    font-size: 1rem;
    padding-top: 5px;
    line-height: 0.3rem;
    font-family: Manrope, sans-serif;
  }
</style>
