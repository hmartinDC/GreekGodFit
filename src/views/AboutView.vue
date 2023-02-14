<script>
export default {
  data() {
    return {
      email: "",
      question: "",
    };
  },
  methods: {
    add() {
      const addQues = {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          email: this.email,
          question: this.question,
        }),
      };
      fetch("http://localhost:3000/Questions", addQues).then((response) =>
        response.json()
      );
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="row">
      <h1 class="d-flex justify-content-around mb-5" style="color: white">
        GREEK GOD FIT
      </h1>
    </div>
    <div class="row mt-3 mb-5" style="color: white">
      <div class="col">
        <h4 class="d-flex">¿Que es Greek God Fit?</h4>
        <p>Una página creada por gente del fitness para gente fitness</p>
        <p>
          Donde encontrar material, ropa y planes de entrenamiento y nutrición
        </p>
      </div>
      <div class="col">
        <div class="d-flex">
          <div class="col">
            <div class="mb-3">
              <label for="exampleFormControlInput1" class="form-label"
                >Email address</label
              >
              <input
                v-model="this.email"
                type="email"
                class="form-control"
                id="exampleFormControlInput1"
                placeholder="name@example.com"
              />
            </div>
            <div class="mb-3">
              <label for="exampleFormControlTextarea1" class="form-label"
                >Escriba lo que quieras saber</label
              >
              <textarea
                v-model="this.question"
                class="form-control"
                id="exampleFormControlTextarea1"
                rows="3"
              ></textarea>
              <button class="btn btn-dark mt-4" @click="add()">Enviar</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
