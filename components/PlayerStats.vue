<template>
  <div class="bg-[#101010] grid p-4 m-6 text-white">
    <div class="flex justify-between gap-10">
      <figure>hi</figure>
      <div class="grid">
        <div class="flex justify-between py-2 border-t-2 border-b-2 border-y-white">
          <p>PAC</p>
          <!-- <p>{{ playerStats.pace.average }}</p> -->
        </div>
        <div class="flex gap-4 py-2">
          <p>Acceleration</p>
          <p class="font-semibold">{{ playerStats.pace.acceleration }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Sprint Speed</p>
          <p class="font-semibold">{{ playerStats.pace.sprintSpeed }}</p>
        </div>
      </div>
      <div class="grid">
        <div class="flex justify-between py-2 border-t-2 border-b-2 border-y-white">
          <p>SHO</p>
          <!-- <p>{{ playerStats.shooting.average }}</p> -->
        </div>
        <div class="flex gap-4 py-2">
          <p>Positioning</p>
          <p class="font-semibold">{{ playerStats.shooting.positioning }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Finishing</p>
          <p class="font-semibold">{{ playerStats.shooting.finishing }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Long Shots</p>
          <p class="font-semibold">{{ playerStats.shooting.longShot }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Penalties</p>
          <p class="font-semibold">{{ playerStats.shooting.penalties }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Shot Power</p>
          <p class="font-semibold">{{ playerStats.shooting.shotPower }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Volleys</p>
          <p class="font-semibold">{{ playerStats.shooting.volleys }}</p>
        </div>
      </div>
      <div class="grid">
        <div class="flex justify-between py-2 border-t-2 border-b-2 border-y-white">
          <p>PAS</p>
          <!-- <p>{{ playerStats.passing.average }}</p> -->
        </div>
        <div class="flex gap-4 py-2">
          <p>Crossing</p>
          <p class="font-semibold">{{ playerStats.passing.crossing }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Curve</p>
          <p class="font-semibold">{{ playerStats.passing.curve }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Free Kick</p>
          <p class="font-semibold">{{ playerStats.passing.freeKick }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Long Passing</p>
          <p class="font-semibold">{{ playerStats.passing.longPassing }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Short Passing</p>
          <p class="font-semibold">{{ playerStats.passing.shortPassing }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Vision</p>
          <p class="font-semibold">{{ playerStats.passing.vision }}</p>
        </div>
      </div>
      <div class="grid">
        <div class="flex justify-between py-2 border-t-2 border-b-2 border-y-white">
          <p>DRI</p>
          <!-- <p>{{ playerStats.dribbling.average }}</p> -->
        </div>
        <div class="flex gap-4 py-2">
          <p>Agility</p>
          <p class="font-semibold">{{ playerStats.dribbling.agility }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Balance</p>
          <p class="font-semibold">{{ playerStats.dribbling.balance }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Ball Control</p>
          <p class="font-semibold">{{ playerStats.dribbling.ballControl }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Composure</p>
          <p class="font-semibold">{{ playerStats.dribbling.composure }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Dribbling</p>
          <p class="font-semibold">{{ playerStats.dribbling.dribbling }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Reactions</p>
          <p class="font-semibold">{{ playerStats.dribbling.reactions }}</p>
        </div>
      </div>
      <div class="grid">
        <div class="flex justify-between py-2 border-t-2 border-b-2 border-y-white">
          <p>DEF</p>
          <!-- <p>{{ playerStats.defense.average }}</p> -->
        </div>
        <div class="flex gap-4 py-2">
          <p>Defensive Awareness</p>
          <p class="font-semibold">{{ playerStats.defense.defAwareness }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Heading</p>
          <p class="font-semibold">{{ playerStats.defense.heading }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Interceptions</p>
          <p class="font-semibold">{{ playerStats.defense.interceptions }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Sliding Tackles</p>
          <p class="font-semibold">{{ playerStats.defense.slidingTackle }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Standing Tackles</p>
          <p class="font-semibold">{{ playerStats.defense.standingTackle }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Standing Tackles</p>
          <p class="font-semibold">{{ playerStats.defense.standingTackle }}</p>
        </div>
      </div>
      <div class="grid">
        <div class="flex justify-between py-2 border-t-2 border-b-2 border-y-white">
          <p>PHY</p>
          <!-- <p>{{ playerStats.physical.average }}</p> -->
        </div>
        <div class="flex gap-4 py-2">
          <p>Aggression</p>
          <p class="font-semibold">{{ playerStats.physical.aggression }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Jumping</p>
          <p class="font-semibold">{{ playerStats.physical.jumping }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Stamina</p>
          <p class="font-semibold">{{ playerStats.physical.stamina }}</p>
        </div>
        <div class="flex gap-4 py-2">
          <p>Strength</p>
          <p class="font-semibold">{{ playerStats.physical.strength }}</p>
        </div>
      </div>
    </div>
    <div>hellooo</div>
  </div>
</template>
<script>
export default {
  name: 'PlayerStats',
  props: [ 'playerStats' ],
  mounted() {
    console.log(this.playerStats);
  }
}
</script>
