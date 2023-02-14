<template>
  <div class="container-fluid">
    <!-- CARRUSEL -->
    <div class="row mb-5">
      <div id="carouselExample" class="carousel slide">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="../images/carrusel1_1.png" class="w-50 mx-auto d-block" />
          </div>
          <div class="carousel-item">
            <img src="../images/carrusel1.jpg" class="w-50 mx-auto d-block" />
          </div>
          <div class="carousel-item">
            <img src="../images/carrusel2.jpg" class="w-50 mx-auto d-block" />
          </div>
          <div class="carousel-item">
            <img src="../images/carrusel3.jpg" class="w-50 mx-auto d-block" />
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExample"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExample"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
    <!-- CARDS -->
    <div class="row p-5 d-flex justify-content-around bg-black">
      <div class="col d-flex align-items-center justify-content-center">
        <div
          class="card d-flex align-items-center justify-content-center"
          style="width: 18rem"
        >
          <img src="../images/camisetas.jpg" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">Clothes</h5>
            <router-link to="Clothe" class="btn btn-dark">Clothes</router-link>
          </div>
        </div>
      </div>
      <div class="col d-flex align-items-center justify-content-center">
        <div
          class="card d-flex align-items-center justify-content-center"
          style="width: 18rem"
        >
          <img src="../images/about.jpg" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">About us</h5>
            <router-link to="About" class="btn btn-dark">About us</router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
