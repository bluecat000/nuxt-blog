<template>
  <div class="content">
      <section class="left-sec">
        <form role="form"> 
          <div class="form-group"> 
            <!-- <textarea id="articel" class="form-control" :value="text" @input="text = $event.target.value"></textarea>  -->
            <textarea id="articel" class="form-control" :value="text" @input="updateText"></textarea> 
            <!-- @input="updateText()" 不能引用$event 要手动传参 -->
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
  .left-sec{
    float: left;
    form{
      width:100%;
      #articel{
        min-height: 60rem;
      }
    }
    width: 40%;
  }
  .right-sec{
    width: 40%;
    float: right;
  }
}
</style>

