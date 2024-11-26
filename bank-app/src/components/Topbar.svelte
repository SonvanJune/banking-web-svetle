<script>
  // Logic cho header nếu cần
  let imageUrl = "../../public/img/vn-flag.jpg";
</script>

<!-- HTML content -->
<div class="topbar">
  <div class="container-fluid">
    <div class="row">
      <div class="col-md-6">
        <div class="left-menu">
          <a class="item active" href="/">Personal Banking</a>
          <a class="item" href="/">Institutional Banking</a>
          <a class="item" href="/">Piority Banking</a>
        </div>
      </div>
      <div class="col-md-6">
        <div class="right-menu">
          <a class="item" href="/">About</a>
          <a class="item" href="/">News</a>
          <a class="item" href="/">Investors</a>
          <a class="item" href="/">Networks</a>
          <a class="item" href="/">Careers</a>
          <a class="item" href="/"
            ><i class="bi bi-telephone-fill"></i>1900 545413</a
          >
          <div class="flag"><img src={imageUrl} alt="" srcset="" /></div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .topbar {
    border-bottom: 0.5px solid #ccc;
    top: 0;
    width: 100%;
    padding-bottom: 10px;
    padding-top: 10px;
  }
  .left-menu {
    display: flex;
    justify-content: flex-start;
    flex-direction: row;
  }

  .right-menu {
    display: flex;
    justify-content: flex-end;
    flex-direction: row;
  }

  .item {
    margin-right: 15px;
    color: #333;
    text-decoration: none;
    font-weight: 500;
    font-size: 1em;
    padding: 2px 5px;
    transition: all 0.8s;
    border-radius: 5px;
    color: #fff;
  }

  .item.active {
    color: #074c31 !important;
    background: #fff !important;
  }

  .item:hover {
    color: #074c31 !important;
    background: #f5f5f5 !important;
  }

  .right-menu .item i {
    margin-right: 5px;
  }

  .right-menu .flag img {
    width: 40px;
    height: 30px;
  }

  .right-menu .flag img:hover{
    cursor: pointer;
  }
</style>
