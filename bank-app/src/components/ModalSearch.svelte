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
      <h3>Search</h3>
      <button on:click={turnOff}><i class="bi bi-x"></i></button>
    </div>
    <div class="modal-content">
      <div class="search">
        <SearchBar
          handleClick={handleClickSearch}
          placeholder="Search here,..."
          width="100%"
          m_top= 0
        ></SearchBar>
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
    height: 85%;
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
    text-align: center;
    padding: 5px;
    border-bottom: 1px solid #ddd;
  }

  .modal-search .search-container button {
    position: absolute;
    background-color: transparent;
    border: none;
    cursor: pointer;
    color: #000;
    font-size: 2em;
    top: 0;
    right: 2%;
  }

  .modal-search .search-container .modal-content .search{
    padding: 20px;
  }
</style>
