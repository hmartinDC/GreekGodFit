<template>
  <nav
    class="navbar navbar-expand-lg justify-content-center fixed-top border-bottom"
    data-bs-theme="dark"
  >
    <div class="container-fluid">
      <a class="navbar-brand" href="Home">
        <img
          src="../images/casco_Logo.png"
          alt="Logo"
          width="30"
          height="24"
          class="d-inline-block align-text-top"
        />
        Greek God Fit
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div
        class="collapse navbar-collapse text-align"
        id="navbarSupportedContent"
      >
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link to="/home" class="nav-link active">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/clothe" class="nav-link active"
              >Clothes
            </router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link active" to="/about"
              >Contact Us</router-link
            >
          </li>
          <li class="nav-item">
            <router-link class="nav-link active" to="/questions"
              >My questions</router-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style>
.navbar-expand-lg {
  background-color: black;
  color: white;
}
.nav-link:hover {
  text-decoration: underline;
}
</style>
