<template>
  <div class="index">
    <Act />
    <Search />
  </div>
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
>div{
  -moz-box-flex: 1 
}
.search{
  margin-left: 3rem;
}
</style>
