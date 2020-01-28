<template>
  <div class="menu">
    <div>Lastest</div>
    <div>Top 10</div>
    <div>Flop 10</div>
    <div>Contribute</div>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.menu {
  display: flex;
  justify-content: center;
}
.menu div{
  width: 10%;
}
</style>
