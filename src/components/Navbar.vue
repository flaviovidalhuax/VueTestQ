<template>
  <nav class="navbar navbar-expand-lg background-primary bg-body-tertiary ">
    <div class="container">
      <a class="navbar-brand " href="#">
        <v-img :width="50" aspect-ratio="1/1" cover :src="this.imagenl"></v-img>
      </a>
      <!-- vuetify.svg -->
      <button
        class="navbar-toggler bg-white"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
       <i class="fas fa-house-damage bg-white"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto gap-5">
          <li class="nav-item">
            <a class="nav-link text-blue" href="#aboutus">About me</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-blue" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-blue" aria-current="page" href="#skill">Skill</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-blue" aria-current="page" href="#footer">Contact me </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
    data() {
    return {
      imagenl: "/src/assets/imagenes/vuetify.svg",
    };
  },
};
</script>

<style scoped>
* {
  font-size: 1.2rem;
  padding: 0;
}
</style>