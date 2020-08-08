<template>
  <div class="graphicList">
    <h1>{{ msg }}</h1>
    <h1>graphic</h1>
  </div>
</template>

<script>
export default {
  name: "GraphicList",
  props: {
    msg: String,
  },
};
</script>