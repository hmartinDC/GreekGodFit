<script>
export default {
  data() {
    return {
      question: [],
      allQuestion: [],
      idS: "",
      idD: "",
      idE: "",
      newQuestion: "",
    };
  },
  methods: {
    async selectOne() {
      const res = await fetch(
        `http://localhost:3000/Questions/`.concat(this.idS)
      );
      this.question = await res.json();
    },
    async editQ() {
      fetch(`http://localhost:3000/Questions/`.concat(this.idE), {
        method: "PATCH",
        headers: {
          "Content-Type": "application/json",
        },
        body: JSON.stringify({ question: this.newQuestion }),
      });
      console.log(this.newQuestion);
    },
    async allQ() {
      const res = await fetch(`http://localhost:3000/Questions`);
      this.allQuestion = await res.json();
    },
    async deleteOne() {
      fetch(`http://localhost:3000/Questions/`.concat(this.idD), {
        method: "delete",
      }).then(this.allQ());
    },
  },
};
</script>
<template>
  <div class="container" style="background: gray">
    <div class="row">
      <div
        class="col d-inline d-flex flex-column justify-content-around align-self-start mb-3"
      >
        <button class="btn btn-dark mt-4 mr-3" @click="selectOne">
          Selection a comment
        </button>
        <input
          v-model="this.idS"
          type="email"
          class="form-control d-flex mt-3"
          id="selectID"
          placeholder="write an id"
        />
        <div>
          <div class="card" v-if="this.question != ''">
            <div class="card-body">
              {{ this.question.email }} <br />
              {{ this.question.question }}
            </div>
          </div>
        </div>
      </div>
      <div
        class="col d-inline d-flex flex-column justify-content-around align-self-start mb-3"
      >
        <button class="btn btn-dark mt-4" @click="allQ">All questions</button>
        <div v-for="questionAll in allQuestion" :key="questionAll.id">
          <div class="card d-flex mt-2 mb-2">
            <div class="card-body">
              {{ questionAll.id }} <br />
              {{ questionAll.email }} <br />
              {{ questionAll.question }}
            </div>
          </div>
        </div>
      </div>
      <div
        class="col d-inline d-flex flex-column justify-content-around align-self-start mb-3"
      >
        <button class="btn btn-dark mt-4" @click="editQ">Edit</button>
        <input
          v-model="this.idE"
          type="email"
          class="form-control d-flex mt-3"
          id="selectID"
          placeholder="write an id"
        />
        <input
          v-model="this.newQuestion"
          type="email"
          class="form-control d-flex mt-2"
          id="selectID"
          placeholder="Rewrite the question"
        />
      </div>
      <div
        class="col d-flex flex-column justify-content-around align-self-start mb-3"
      >
        <button class="btn btn-dark mt-4" @click="deleteOne">Delete</button>
        <input
          v-model="this.idD"
          type="email"
          class="form-control d-flex mt-3"
          id="deleteID"
          placeholder="write an id"
        />
      </div>
    </div>
  </div>
</template>
