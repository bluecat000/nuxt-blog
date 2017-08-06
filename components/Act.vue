<template>
  <div class="act">
    <div class="row">
      <div class="col-sm-6 col-md-4" v-for="list in 10">
        <div class="thumbnail">
          <!-- <img :src="img" alt="...">  -->
          <div class="caption">
            <h3>标题</h3>
            <p>描述</p>
          </div>
        </div>
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
