<template>
  <Main msg="Vue 3 test" />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import Main from '../components/Main.vue'

export default defineComponent({
  components: {
    Main,
  },
})
</script>
