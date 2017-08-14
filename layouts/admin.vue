<template>
  <div>
    <header>
      <nav class="navbar navbar-inverse navbar-fixed-top">
        <div class="container-fluid">
          <!-- Brand and toggle get grouped for better mobile display -->
          <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
              <span class="sr-only">Toggle navigation</span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
            </button>
            <nuxt-link  class="navbar-brand" to="/admin/admin">BCblog</nuxt-link>
          </div>

          <!-- Collect the nav links, forms, and other content for toggling -->
          <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
              <li class="active"><a href="#">View<span class="sr-only">(current)</span></a></li>
              <li><a href="#">github</a></li>
              <li class="dropdown">
                <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">NEW<span class="caret"></span></a>
                <ul class="dropdown-menu">
                  <li><nuxt-link to="/admin/edit">Create Bolg</nuxt-link></li>
                  <li role="separator" class="divider"></li>
                  <li><a href="#">Create folder</a></li>
                </ul>
              </li>
            </ul>            
          </div><!-- /.navbar-collapse -->
        </div><!-- /.container-fluid -->
      </nav>
    </header>
    <section class="container">
      <nuxt/>
    <Search />
  </section>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
.container-fluid{
  max-width: 1020px;
}
.container{
  position: relative;
  top: 80px;
//   max-width: 1040px;
  display: -webkit-box;
}
</style>
