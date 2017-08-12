<template>
    <div class="articel">
        <div class="art-main">
            <p class="lead">
                Nullam quis risus eget urna mollis ornare vel eu leo. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nullam id dolor id nibh ultricies vehicula.

                Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec ullamcorper nulla non metus auctor fringilla. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Donec ullamcorper nulla non metus auctor fringilla.

                Maecenas sed diam eget risus varius blandit sit amet non magna. Donec id elit non mi porta gravida at eget metus. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit.
            </p>
        </div>
        <Search />
    </div>
</template>

<script>
import Search from '~/components/Search.vue'

const axios = require('axios')

export default {
  created: () => {
    axios.get('/markdown/README.md')
  },
  components: {
    Search
  }
}
</script>

<style lang="scss">
.art-main{
    display: inline-block;
    max-width: 640px;
}
</style>

