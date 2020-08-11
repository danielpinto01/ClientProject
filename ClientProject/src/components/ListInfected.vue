<template>
  <!-- <div class="listInfected">
    <h1>{{ msg }}</h1>
    <table class="table table-dark">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Nombre</th>
          <th scope="col">Ubicacion</th>
          <th scope="col">Url foto</th>
          <th scope="col">Fecha</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Richard</td>
          <td>Villao</td>
          <td>Soyunaputa.png</td>
          <td>08/05/20</td>
        </tr>
      </tbody>
    </table>

     <button type="btnPDFList" class="btn btn-outline-success">Print PDF</button>

  </div>-->

  <div class="container">
    <h1>Lista de contagios</h1>
    <iframe
      src="https://docs.google.com/viewer?srcid=1H0eMUfBH-mewGDnAvkX-I1m1DC65SNqZ&pid=explorer&efh=false&a=v&chrome=false&embedded=true"
      width="50%"
      height="550px"
    ></iframe>
    <div class="row">
      <div class="mx-auto">
        <button type="btnPDFList" class="btn btn-outline-success">Print PDF</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ListInfected",
  props: {
    msg: String,
  },
};
</script>