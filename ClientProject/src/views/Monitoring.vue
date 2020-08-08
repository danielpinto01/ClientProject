<template>
  <div class="monitoring">
      <SystemMonitoring msg="monitoreo"/>
  </div>
</template>

<script>
import SystemMonitoring from '@/components/SystemMonitoring.vue'

export default {
  name: 'Monitoring',
  components: {
    SystemMonitoring
  }
}
</script>

<style scoped>
</style>