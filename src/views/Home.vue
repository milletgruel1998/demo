<template>
  <div class="home">
    <h2>我是Home页面</h2>
  </div>
</template>

<script>
export default {
  created () {
    console.log(this.$route.params.name)
  }
}
</script>

<style>
</style>
