<template>
  <div class="container">
    <div class="row">
      <div class="right_list col-lg-4 col-md-3 col-md-push-9 col-lg-push-8">2</div>
      <div class="left_list col-lg-8 col-md-9 col-md-pull-3 col-lg-pull-4">
        <articlelist />
      </div>
    </div>
  </div>
</template>

<script>
import articlelist from '@/components/articlelist.vue'
export default {
  components: {
    articlelist
  }
}
</script>

<style lang="scss" scoped>
.container {
  margin-top: 25px;
  margin-bottom: 20px;
}
// .row {
//   display: flex;
// }
.right_list {
  background: blueviolet;
  height: 100vh;
}
.left_list {
}
</style>