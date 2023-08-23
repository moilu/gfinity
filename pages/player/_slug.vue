<template>
  <div class="bg-black h-screen overflow-auto md:mx-auto pb-2 md:px-0 w-full md:w-[90%] 2xl:w-[55%]">
    <PlayerStats :playerStats="statistics" />
  </div>
</template>
<script>
import { client } from '../../sanity.js'

export default {
  data() {
    return {
      playerInfo: [],
      statistics: []
    }
  },
  methods: {
    async getPosts() {
      const playerInfo = await client.fetch(`*[slug.current == "${this.$route.params.slug}"]`);
      return playerInfo
    }
  },
  async mounted() {
    this.playerInfo = await this.getPosts();
    this.statistics = this.playerInfo[0].statistics
    console.log(this.playerInfo)
  }
}
</script>
