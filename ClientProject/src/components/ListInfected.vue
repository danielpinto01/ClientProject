<template>
  <div class="container">
    <h1>Reporte de contagios</h1>

    <div class="row">
      <div class="mx-auto">
        <button 
          v-on:click="requestPDFLink"
          type="btnRegisterPerson"
          class="btn btn-outline-success"
        >Actualizar Reporte</button>
      </div>
    </div>
    <iframe style="margin-top:10px;" v-bind:src="pdfSrc" width="50%" height="550px"></iframe>
  </div>
</template>

<script>
export default {
  name: "ListInfected",
  props: {
    msg: String,
  },
  data: function () {
    return {
      pdfSrc: "",
    };
  },
  methods: {
    requestPDFLink: function () {
      axios({ method: "get", url: "http://localhost:3000/reports/generatePDF" })
        .then((response) => {
          this.pdfSrc = "http://" + response.data;
          console.log(this.pdfSrc);
        })
        .catch(function (err) {
          console.log(err);
        });
    },
  },
};
</script>