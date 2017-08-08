<template>
  <div class="act">
    <div class="row">
      <div class="panel panel-default" v-for="list in 10" v-bind:key="list">
        <!-- Default panel contents -->
        <nuxt-link to="/articel">
          <div class="panel-heading">Panel heading</div>
            <div class="panel-body">
              <p>Some default panel content here. Nulla vitae elit libero, a pharetra augue. Aenean lacinia bibendum nulla sed consectetur. Aenean eu leo quam.</p>
            </div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      img: require('~/static/logo.png')
    }
  }
}
</script>

<style lang="scss">
.act{
  display: inline-block;
  max-width: 640px;
}
.row{
  margin: 0;
}
.col-sm-6{
  width: 100%;
  .thumbnail{
    border-right: none;
    border-top: none;
    border-left: none;
    display: -webkit-box;
    img{
      width: 130px;
      height: 130px;
      flex: 1;
      margin: 0;
      vertical-align: middle;
    }
    h3{
      margin-top: 0;
    }
     .caption{
       flex: 999;
    }
  }
}
.col-sm-6:last-child{
  .thumbnail{
    border: none;
  }
}
</style>
