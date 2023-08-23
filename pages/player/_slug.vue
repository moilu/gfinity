<template>
  <div>
    hi
  </div>
</template>
<script>
import { client } from '../../sanity.js'

export default {
  data() {
    return {
      fifaCards: []
    }
  },
  methods: {
    async getPosts() {
      const fifaCards = await client.fetch('*[_slug == "aaron-ramsey-rangers-80-ovr"]');
      return fifaCards
    }
  },
  async created() {
    this.fifaCards = await this.getPosts();
  }
}
</script>
