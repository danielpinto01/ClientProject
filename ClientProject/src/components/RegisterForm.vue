<template>
  <div class="init">
    <h1>{{ msg }}</h1>
    <div class="container mydiv">
      <form>
        <div class="form-group">
          <label>Nombre:</label>
          <input v-model="name" class="form-control" id="inputName" />
        </div>
        <div class="form-group">
          <label>Ciudad:</label>
          <input v-model="city" class="form-control" id="inputCity" />
        </div>
        <form>
          <div class="form-group">
            <label>Agregar foto:</label>
            <div class="row">
              <div class="mx-auto">
                <input type="file" class="form-control-file" id="inputPhoto" ref="file" />
              </div>
            </div>
          </div>
        </form>
        <button
          v-on:click="sendData"
          type="btnRegisterPerson"
          class="btn btn-outline-success"
        >Registrar contagio</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "RegisterForm",
  props: {
    msg: String,
  },
  data() {
    return {
      name: "",
      city: "",
      file: "",
      showAlert: false,
    };
  },
  methods: {
    sendData: function () {
      console.log(new Date());
      var formData = new FormData();
      formData.set("name", this.name);
      formData.set("city", this.city);
      formData.set("date_contagion", new Date().toDateString());
      var file = this.$refs.file.files[0];
      formData.append("image", file);
      axios({
        method: "post",
        url: "http://localhost:3000/contagions/add",
        data: formData,
        headers: { "Content-Type": "multipart/form-data" },
      })
        .then(function (response) {
          console.log(response.data);
          alert('Agregado correctamente')
        })
        .catch(function (response) {
          console.log(response.data);
          alert('FALLO: ' + response.mesage)
        });
    },
  },
};
</script>