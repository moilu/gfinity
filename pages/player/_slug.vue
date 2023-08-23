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
      const fifaCards = await client.fetch(`*[_id == "${this.$route.params.id}"]`);
      console.log(this.$route.params.id)
      return fifaCards
    }
  },
  async mounted() {
    this.fifaCards = await this.getPosts();
  }
}
</script>
