<template>
  <Link href="/">Main Page</Link>&nbsp;
  <Link href="/hello">Show Page</Link>
  <Link href="/listing">Listings</Link>
  <Link href="/listing/create">Add Listing</Link>
  <!-- <div>The page with time {{ timer }}</div> -->
  <div v-if="flashSuccess" class="success">
    {{ flashSuccess }}
  </div>
  <slot>Default</slot>
</template>

<script setup>
import {Link, usePage} from '@inertiajs/vue3'
import { computed } from 'vue'

//access flash message data
const flashSuccess = computed(() => usePage().props.flash.success)

// import {ref} from 'vue'
// const timer = ref(0)
// setInterval(()=> timer.value++, 1000)
</script>

<style scoped>
  .success {
    background-color: green;
    color: white;
  }

</style>
