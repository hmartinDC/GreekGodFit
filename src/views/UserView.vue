<script>
export default {
  data() {
    return {
      userNameR: "",
      emailR: "",
      passR: "",
      userL: "",
      passL: "",
    };
  },
  methods: {
    async logIn() {
      alert("Buenas" + " " + this.userL);

      document.cookie = "user="+this.userL;
      document.cookie = "password="+this.passL;
      alert(document.cookie)
    },
    addUser() {
      const addUser = {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          username: this.userNameR,
          email: this.emailR,
          password: this.passR,
        }),
      };
      fetch("http://localhost:3000/users", addUser).then((response) =>
        response.json()
      );
      alert("Te has registrado" + " " + this.userNameR);
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="row">
      <!-- COLUMNA CON EL INICIO DE SESION -->
      <div class="col">
        <h3 class="d-flex justify-content-around" style="color: white">
          Inicio de Sesión
        </h3>
        <div class="mb-3 row">
          <label class="col-sm-2 col-form-label" style="color: white"
            >Username</label
          >
          <div class="col-sm-10">
            <input
              v-model="userL"
              type="text"
              class="form-control-plaintext"
              style="color: white"
              placeholder="xxTentacion"
            />
          </div>
        </div>
        <div class="mb-3 row">
          <label
            for="inputPassword"
            class="col-sm-2 col-form-label"
            style="color: white"
            >Password</label
          >
          <div class="col-sm-10">
            <input
              v-model="passL"
              type="password"
              class="form-control-plaintext"
              style="color: white"
              placeholder="INTRODUZCA CONTRASEÑA"
            />
          </div>
        </div>
        <div class="d-flex justify-content-around">
          <button class="btn btn-dark mb-3" @click="logIn">Log In</button>
        </div>
      </div>
      <!-- COLUMNA CON EL REGISTRO -->
      <div class="col">
        <h3 class="d-flex justify-content-around" style="color: white">
          Registro de usuario
        </h3>
        <div class="mb-3 row">
          <label
            for="staticEmail"
            class="col-sm-2 col-form-label"
            style="color: white"
            >UserName</label
          >
          <div class="col-sm-10">
            <input
              v-model="userNameR"
              type="text"
              class="form-control-plaintext"
              style="color: white"
              placeholder="xxTentacion"
            />
          </div>
        </div>
        <div class="mb-3 row">
          <label
            for="staticEmail"
            class="col-sm-2 col-form-label"
            style="color: white"
            >Email</label
          >
          <div class="col-sm-10">
            <input
              v-model="emailR"
              type="text"
              class="form-control-plaintext"
              placeholder="email@example.com"
              style="color: white"
            />
          </div>
        </div>
        <div class="mb-3 row">
          <label
            for="inputPassword"
            class="col-sm-2 col-form-label"
            style="color: white"
            >Password</label
          >
          <div class="col-sm-10">
            <input
              v-model="passR"
              type="password"
              class="form-control-plaintext"
              style="color: white"
              placeholder="INTRODUZCA CONTRASEÑA"
            />
          </div>
        </div>
        <div class="d-flex justify-content-around">
          <button class="btn btn-dark mt-2 mb-3" @click="addUser">Register</button>
        </div>
      </div>
    </div>
  </div>
</template>
