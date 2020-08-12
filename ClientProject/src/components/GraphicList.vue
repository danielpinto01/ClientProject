<template>
  <div class="container-fluid">
    <div class="graphicList">
      <h1>Casos por ciudad</h1>
      <!--chartjs-bar v-bind:labels="labels" v-bind:datasets="datasets" v-bind:option="option"></chartjs-bar-->
      <chartjs-doughnut v-bind:labels="labels"  v-bind:datasets="datasets" v-bind:option="option" :options="{responsive: true, maintainAspectRatio: false}"></chartjs-doughnut>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      labels: ["Sun", "Mon", "Tue"],
      datasets: [
        {
          data: [20, 30, 50],
          backgroundColor: ["#f36e60", "#ffdb3b", "#185190"],
        },
      ],
      option: {
        title: {
          display: true,
          position: "top",
          text: "Contagios en Colombia",
        },
      },
    };
  },
  created: function () {
    this.requestData();
  }, 
  methods: {
    requestData: function () {
      this.labels = [];
      this.datasets[0].data = [];
      this.datasets[0].backgroundColor = [];
      axios({ method: "get", url: "http://localhost:3000/reports/contagionsByCity" })
        .then((response) => {
          response.data.forEach((element) => {
            this.addElement(element);
          });
        })  
        .catch(function (err) {
          console.log(err);
        });
    },
    addElement: function (element) {
      this.labels.push(element.name);
      this.datasets[0].data.push(element.count);
      this.datasets[0].backgroundColor.push(
        "#" + (((1 << 24) * Math.random()) | 0).toString(16)
      );
    },
  },
};
</script>

<style scoped>
.graphicList {
  padding-left: 15%;
  padding-right: 15%;
}
</style>