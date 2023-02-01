<template>
  <h1>Index</h1>
  <Link href="/hello">Show Page</Link>
  <div>
    The message is {{ message }}
  </div>
</template>

<script setup>
import {Link} from '@inertiajs/vue3'
defineProps({message: String})
</script>


<!-- If I want to use a different layout define it with the code below -->
<!-- <script>
    import LayoutTwo from '../../Layouts/LayoutTwo.vue'
    export default {
        layout: LayoutTwo
    }
</script> -->
