<template>
  <div>
    <button>
      <slot name="text">Envoyer</slot>
    </button>
  </div>
</template>

<script>

export default {
  name: 'Button',
  props: {
    action: String,
    qotd: Object
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
