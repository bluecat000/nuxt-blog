<template>
  <div class="search">
    <div class="form-group">
      <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
    </div>
    <div class="list-search">
      <ul class="nav nav-tabs">
        <li role="presentation" class="active"><a href="#">Home</a></li>
        <li role="presentation"><a href="#">Profile</a></li>
        <li role="presentation"><a href="#">Mages</a></li>
        <li role="presentation"><a href="#">Mges</a></li>
      </ul>
      <div class="list-group">
        <a href="#" class="list-group-item active">
            Cras justo odio
        </a>
        <a href="#" class="list-group-item">Dapibus ac facilisis in</a>
        <a href="#" class="list-group-item">Morbi leo risus</a>
        <a href="#" class="list-group-item">Porta ac consectetur ac</a>
        <a href="#" class="list-group-item">Vestibulum at eros</a>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.search{
  width: 250px;
  float: right;
  display: inline-block;
  .form-group{
    margin: 0 0 .3rem 0;
  }
  .input-group{
    // margin-bottom: .5rem;
  }
  .nav.nav-tabs{
      display: -webkit-box;
      li{
          -webkit-box-flex: 1;
      }
  }
}
</style>
