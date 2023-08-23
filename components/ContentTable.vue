<template>
<div class="h-screen overflow-auto md:mx-auto pb-2 md:px-0 w-full md:w-[90%] 2xl:w-[55%]">
  <table class="relative w-full text-white">
    <thead class="sticky top-0 bg-black">
        <tr>
          <template v-for="(header, idx) in table_headers">
            <th :key="idx" class="px-6 py-4 text-sm font-semibold text-center">
              <div class="flex items-center gap-1">
                {{ header }}
                <img src="../static/group.svg" alt="group svg icon">
              </div>
            </th>
          </template>
        </tr>
    </thead>
    <tbody>
        <template v-for="(card, idx) in fifaCards">
          <tr :key="idx" class="bg-[#101010] border-b border-black">
            <NuxtLink :to="{ path: '/player/' + card.slug.current, params: { id: card._id }}" >
              <td class="px-6 py-4 font-medium whitespace-nowrap">{{ card.name }}</td>
            </NuxtLink>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center text-black bg-white rounded">{{ card.rating }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center bg-black rounded">{{ card.position }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center bg-black rounded">{{ card.position }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center border border-white rounded">{{ card.statistics.pace.average }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center border border-white rounded">{{ card.statistics.shooting.average }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center border border-white rounded">{{ card.statistics.passing.average }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center border border-white rounded">{{ card.statistics.dribbling.average }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center border border-white rounded">{{ card.statistics.defense.average }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center border border-white rounded">{{ card.statistics.physical.average }}</div>
            </td>
            <td class="px-6 py-4 whitespace-nowrap">
              <div class="p-1 text-center bg-black rounded">{{ `${card.workRatesAttacking[0]} / ${card.workRatesDefensive[0]}` }}</div>
            </td>
          </tr>
        </template>
          </tbody>
  </table>
</div>
</template>
<script>
import { client } from '../sanity.js'

export default {
  name: 'ContentTable',
  data() {
    return {
      table_headers: [
        'Name',
        'OVR',
        'POS',
        'Type',
        'PAC',
        'SHO',
        'PAS',
        'DRI',
        'DEF',
        'PHY',
        'WR'
      ],
      fifaCards: []
    }
  },
  methods: {
    async getPosts() {
      const fifaCards = await client.fetch('*[_type == "fifaCard"]');
      return fifaCards
    }
  },
  async created() {
    this.fifaCards = await this.getPosts();
  }
}

</script>
