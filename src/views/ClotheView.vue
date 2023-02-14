<template>
  <div class="row p-5 d-flex justify-content-around bg-black">
    <div class="col d-flex align-items-center justify-content-center">
      <div
        class="card d-flex align-items-center justify-content-center"
        style="width: 18rem"
      >
        <img src="../images/camisetas.jpg" class="card-img-top" />
        <div id="tshirt" class="card-body">
          <h5 class="card-title">Camiseta</h5>
          <router-link
            to="article/1"
            class="btn btn-dark d-flex justify-content-around"
            >Ver</router-link
          >
        </div>
      </div>
    </div>
    <div class="col d-flex align-items-center justify-content-center">
      <div
        class="card d-flex align-items-center justify-content-center"
        style="width: 18rem"
      >
        <img src="../images/sudadera.jpg" class="card-img-top" />
        <div id="tshirt" class="card-body">
          <h5 class="card-title">Sudadera</h5>
          <router-link
            to="article/2"
            class="btn btn-dark d-flex justify-content-around"
            >Ver</router-link
          >
        </div>
      </div>
    </div>
  </div>
  <div class="row p-5 d-flex justify-content-around bg-black">
    <div class="col d-flex align-items-center justify-content-center">
      <div
        class="card d-flex align-items-center justify-content-center"
        style="width: 18rem"
      >
        <img src="../images/cortos.jpg" class="card-img-top" />
        <div id="pant" class="card-body">
          <h5 class="card-title">Pantalones Cortos</h5>
          <router-link
            to="article/3"
            class="btn btn-dark d-flex justify-content-around"
            >Ver</router-link
          >
        </div>
      </div>
    </div>
    <div class="col d-flex align-items-center justify-content-center">
      <div
        class="card d-flex align-items-center justify-content-center"
        style="width: 18rem"
      >
        <img src="../images/calcetines.jpg" class="card-img-top" />
        <div id="shocks" class="card-body">
          <h5 class="card-title">Calcetines Deadlift</h5>
          <router-link
            to="article/4"
            class="btn btn-dark d-flex justify-content-around"
            >Ver</router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>
