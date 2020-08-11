<template>
  <div class="graphicList">
    <h1>{{ msg }}</h1>
    <h1>graphic</h1>

    <chartjs-doughnut v-bind:labels="labels" v-bind:datasets="datsets" v-bind:option="option"></chartjs-doughnut>
  </div>
</template>

<script>
export default {
 data() {
    return {
      labels: ["Sun", "Mon", "Tue"],
      datasets: [
        {
          data: [20, 30, 50],
          backgroundColor: ["#f36e60", "#ffdb3b", "#185190"]
        }
      ],
      option: {
        title:{
          display:true,
          position: "bottom",
          text: "Fruits"
        }
      }
    };
  }
};
</script>

<style scoped>

</style>