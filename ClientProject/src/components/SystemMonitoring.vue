<template>
  <div class="systemMonitoring">
    <h1>{{ msg }}</h1>
    <h1>moni</h1>
  </div>
</template>

<script>
export default {
  name: "SystemMonitoring",
  props: {
    msg: String,
  },
};
</script>