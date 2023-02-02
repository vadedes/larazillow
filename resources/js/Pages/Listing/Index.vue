<script setup>
import ListingAddress from '@/Components/ListingAddress.vue'
import { Link } from '@inertiajs/vue3'
defineProps({
  listings: Array,
})

</script>
//   adding semi-colon before the key makes it dynamic, and vue will check the
//   variables if there are values associated with the variable given
//   if we don't add semi-colon, then vue will literally assign listing.id to all the elements in the loop
<template>
  <div v-for="listing in listings" :key="listing.id">
    <Link :href="`/listing/${listing.id}`">
      <ListingAddress :listing="listing" />
    </Link>
  </div>
</template>
