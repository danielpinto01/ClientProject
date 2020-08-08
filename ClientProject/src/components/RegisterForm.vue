<template>
  <div class="init">
    <h1>{{ msg }}</h1>
    <div class="container mydiv">
      <form>
        <div class="form-group">
          <label>Nombre:</label>
          <input class="form-control" id="inputName" />
        </div>
        <div class="form-group">
          <label>Ciudad:</label>
          <input class="form-control" id="inputCity" />
        </div>
        <form>
          <div class="form-group">
            <label>Agregar foto:</label>
            <div class="row">
              <div class="mx-auto">
                <input type="file" class="form-control-file" id="inputPhoto" />
              </div>
            </div>
          </div>
        </form>
        <button type="btnRegisterPerson" class="btn btn-outline-success">Registrarse</button>
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
};
</script>