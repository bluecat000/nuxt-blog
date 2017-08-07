<template>
  <section class="container">
    <Act />
    <Search />
  </section>
</template>

<script>
import Act from '~/components/Act.vue'
import Search from '~/components/Search.vue'

export default {
  components: {
    Act,
    Search
  }
}
</script>

<style lang="scss">
.container{
  max-width: 1040px;
  display: -webkit-box;
  >div{
    -moz-box-flex: 1 
  }
  .search{
    margin-left: 3rem;
  }
}
</style>
