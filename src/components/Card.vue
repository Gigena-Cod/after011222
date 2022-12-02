<template>
  <div class="bg-black bg-opacity-50 border rounded p-4 card">
    <div class=" image">
      <img class="mx-auto" :src="monster.profile" :alt="`Image ${monster.name}`" />
    </div>
    <div class="uppercase truncate mt-4 font-bold text-white title">
      {{ monster.name }}
    </div>
    <div class="truncate mt-4 text-sm italic text-white title">
      {{ monster.email }}
    </div>
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  props: {
    monster: Object,
  },
};
</script>

<style lang="scss" scoped></style>
