<template>
<div class="h-screen overflow-auto md:mx-auto pb-2 md:px-0 w-full md:w-[90%] 2xl:w-[55%]">
  <table class="text-white w-full">
    <thead class="bg-black">
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
        <template v-for="(data, idx) in table_data">
          <tr :key="idx" class="bg-[#101010] border-b dark:border-neutral-500">
            <td class="whitespace-nowrap px-6 py-4 font-medium">{{ data.name }}</td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-white rounded p-1 text-black text-center">{{ data.ovr }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-black rounded p-1 text-center">{{ data.pos }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-black rounded p-1 text-center">{{ data.type }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ data.pac }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ data.sho }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ data.pas }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ data.dri }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ data.def }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="border border-white rounded p-1 text-center">{{ data.phy }}</div>
            </td>
            <td class="whitespace-nowrap px-6 py-4">
              <div class="bg-black rounded p-1 text-center">{{ data.wr }}</div>
            </td>
          </tr>
        </template>
          </tbody>
  </table>
</div>
</template>
<script>
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
      table_data: [
        {
          name: 'Lionel Messi',
          ovr: '93',
          pos: 'RW',
          type: 'RW',
          pac: '85',
          sho: '92',
          pas: '91',
          dri: '1',
          def: '1',
          phy: '1',
          wr: '1'
        },
        {
          name: 'Cristiano Ronaldo',
          ovr: '92',
          pos: 'ST',
          type: 'ST',
          pac: '90',
          sho: '93',
          pas: '82',
          dri: '84',
          def: '35',
          phy: '85',
          wr: '2'
        },
        {
          name: 'Neymar Jr.',
          ovr: '91',
          pos: 'LW',
          type: 'LW',
          pac: '91',
          sho: '85',
          pas: '87',
          dri: '92',
          def: '20',
          phy: '58',
          wr: '3'
        }
      ]
    }
  }
}

</script>
