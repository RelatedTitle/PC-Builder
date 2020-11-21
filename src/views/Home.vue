<template>
  <div class="home">
    <Builder/>
  </div>
</template>

<script>
// @ is an alias to /src
import Builder from '@/components/builder.vue'

export default {
  name: 'Home',
  components: {
    Builder
  }
}
</script>
