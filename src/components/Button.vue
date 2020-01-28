<template>
  <div>
    <button v-html="getLabel(action)"></button>
  </div>
</template>

<script>

export default {
  name: 'Button',
  props: {
    action: String,
    qotd: Object
  },
  methods: {
    getLabel: function(type) {
      return type === 'voteplus' ? 'trolol' : 'dafuq'
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
