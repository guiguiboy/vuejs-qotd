<template>
  <div class="qotd_list">
    <div>{{ title }}</div>

    <Qotd v-for="item in getList" v-bind:qotd="item" v-bind:key="item.id">
    </Qotd>
  </div>
</template>

<script>
import Qotd from "./Qotd";

export default {
  name: 'QotdList',
  props: {
    name: String,
    pagination: Boolean,
    limit: Number,
    sortColumn: String,
    sortOrder: String,
  },
  components: {
    Qotd,
  },
  computed:{
    title: function() {
      return this.name.toUpperCase()
    },
    getList: () => {
      //should be retrieved from an API. (axios / fetch, ...)
      return [
        {
          id: 10,
          title: "Lorem Ipsum",
          value: "<user1> Lorem ipsum dolor sit amet\n<user2> Consectetur adipiscing elit\n<user1> Tempor incididunt ut labore",
          score: {
            top: 20,
            flop: 3,
          }
        },
        {
          id: 11,
          title: "Lorem Ipsum 2",
          value: "<user1> Lorem ipsum dolor sit amet\n<user2> Consectetur adipiscing elit\n<user1> Tempor incididunt ut labore",
          score: {
            top: 34,
            flop: 6,
          }
        },
        {
          id: 12,
          title: "Lorem Ipsum 3",
          value: "<user1> Lorem ipsum dolor sit amet\n<user2> Consectetur adipiscing elit\n<user1> Tempor incididunt ut labore",
          score: {
            top: 2,
            flop: 23,
          }
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
