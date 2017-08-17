<template>
  <div class="content">
    <div class="sub-til">
      <span class="sub-til-text">NEW BOLG</span>
      <div class="btn-group">
        <button type="button" class="btn btn-primary">Action</button>
        <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          <span class="caret"></span>
          <span class="sr-only">Toggle Dropdown</span>
        </button>
        <ul class="dropdown-menu">
          <li><a href="#">save</a></li>
          <li role="separator" class="divider"></li>
          <li><a href="#">save in draft</a></li>
        </ul>
      </div>
    </div>
    <section class="left-sec">
      <form role="form"> 
        <div class="form-group"> 
          <!-- <textarea id="articel" class="form-control" :value="text" @input="text = $event.target.value"></textarea>  -->
          <textarea id="articel" class="form-control" :value="text" @input="updateText"></textarea> 
          <!-- @input="updateText()" 如果引用$event 要手动传参 -->
        </div> 
      </form>  
    </section>
    <section class="right-sec" v-html="reflashView"></section>
  </div>
</template>
<script>
const markdown = require('markdown').markdown
export default {
  layout: 'admin',
  data () {
    return {
      text: '# untitle'
    }
  },
  computed: {
    reflashView: function (e) {
      return markdown.toHTML(this.text)
    }
  },
  methods: {
    updateText: function (e) {
      this.text = e.target.value
    }
  }
}
</script>
<style lang="scss" scope>
.content{
  width: 100%;
  .sub-til{
    .sub-til-text{
      font-size: 3rem;
      vertical-align: middle;
      margin-right: 2rem;
    }
  }
  .left-sec{
    padding-top: 2rem;
    float: left;
    form{
      width:100%;
      #articel{
        min-height: 60rem;
      }
    }
    width: 48%;
  }
  .right-sec{
    width: 48%;
    float: right;
  }
}
</style>

