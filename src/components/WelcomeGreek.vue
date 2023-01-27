<template>
  <div class="container-fluid">
    <div class="row">
      <div id="carouselExample" class="carousel slide ">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="../images/carrusel1_1.png" class="w-75 mx-auto d-block"/>
          </div>
          <div class="carousel-item">
            <img src="../images/carrusel1.jpg" class="w-75 mx-auto d-block" />
          </div>
          <div class="carousel-item">
            <img src="../images/carrusel2.jpg" class="w-75 mx-auto d-block" />
          </div>
          <div class="carousel-item">
            <img src="../images/carrusel3.jpg" class="w-75 mx-auto d-block" />
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
  </div>
</template>
