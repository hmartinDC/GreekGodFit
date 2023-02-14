<script>
export default {
  data() {
    return {
      article: [],
    };
  },
  methods: {
    async fetchData() {
      const res = await fetch(
        `http://localhost:3000/Clothe/${this.$route.params.id}`
      );
      this.article = await res.json();
    },
  },
  mounted() {
    this.fetchData();
  },
};
</script>

<template>
  <div class="container card mb-5">
    <div class="row mb-3">
      <div class="col d-flex justify-content-center mt-3">
        <img :src="'/src/images/' + article.id + '.jpg'" style="width: 26rem" />
      </div>
      <div class="col p-4">
        <h3 class="mb-5">{{ article.name }}</h3>
        <select class="form-select d-flex" aria-label="Default select example">
          <option selected>SIZE</option>
          <option
            v-for="(size, index) of article.size"
            :key="index"
            value="{{index}}"
          >
            {{ size }}
          </option>
        </select>
        <h4 class="mt-5">Price:</h4>
        <h5>{{ article.price }}</h5>
      </div>
    </div>
  </div>
</template>
