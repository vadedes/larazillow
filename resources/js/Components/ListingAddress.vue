<script setup>
defineProps({
  listing: Object,
})
</script>

<template>
  <span>
    {{ listing.street_nr }} {{ listing.street }},  {{ listing.city }}, for ${{ listing.price }}
  </span>
</template>