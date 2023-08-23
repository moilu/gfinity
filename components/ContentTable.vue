<template>
<div class="h-screen overflow-auto md:mx-auto pb-2 md:px-0 w-full md:w-[90%] 2xl:w-[55%]">
  <table class="relative text-white w-full">
    <thead class="bg-black sticky top-0">
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
            <NuxtLink to="/player">
              <td class="whitespace-nowrap px-6 py-4 font-medium">{{ card.name }}</td>
            </NuxtLink>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-white rounded p-1 text-black text-center">{{ card.rating }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-black rounded p-1 text-center">{{ card.position }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-black rounded p-1 text-center">{{ card.position }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ card.statistics.pace.average }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ card.statistics.shooting.average }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ card.statistics.passing.average }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ card.statistics.dribbling.average }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ card.statistics.defense.average }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ card.statistics.physical.average }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-black rounded p-1 text-center">{{ `${card.workRatesAttacking[0]} / ${card.workRatesDefensive[0]}` }}</div>
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
      console.log(fifaCards[0])
      return fifaCards
    }
  },
  async created() {
    this.fifaCards = await this.getPosts();
  }
}

</script>
