<template>
  <div class="qotd" :id="getQotdDivId">
    <div>{{ qotd.title }}</div>
    <div v-html="valueToDisplay"></div>
    <div>{{ qotd.score }}</div>
    <Button action="voteplus" :qotd="qotd">
      <template v-slot:text>
        +1
      </template>
    </Button>
    <Button action="voteminus" :qotd="qotd">
      <template v-slot:text>
        -1
      </template>
    </Button>
  </div>
</template>

<script>
import Button from "./Button";

export default {
  name: 'Qotd',
  props: {
    qotd: Object,
  },
  components: {
    Button,
  },
  computed:
  {
    valueToDisplay: function() {
      return this.qotd.value.replace(/</g, '&lt;').replace(/>/g, '&gt;').replace(/\n/g, '<br/>')
    },
    getQotdDivId: function(){
      return `qotd-${this.qotd.id}`
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
