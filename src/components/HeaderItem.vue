<template>
  <div id="jumbotron">
    <div class="bg-white rounded-start p-2 d-flex flex-column align-items-center position-absolute end-0" id="side-menu">
      <a href="#"><i class="fa-solid fa-bars mb-2"></i></a>
      <a href="#"><i class="fa-solid fa-life-ring mb-2"></i></a>
      <a href="#"><i class="fa-solid fa-book mb-2"></i></a>
      <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
    </div>
    <!-- Intestazione con menu di navigazione -->
    <div class="container">
      <header class=" mb-5 py-3 d-flex justify-content-between align-items-center">
        <a href="#"><img id="logo" src="../assets/img/dark-logo.png" alt="Max Coach"></a>
        <nav class="d-flex">
          <ul class="d-flex align-items-center">
            <li v-for="link in links" :key="link.id"
            class="ms-5 fw-semibold">
            <a 
            :href="link.url"
            >{{link.text}} <i class="fa-solid fa-angle-down"></i>
            </a>
            </li>
          </ul>
          <a class="ms-3" href="#"><i class="fa-solid fa-cart-shopping"></i></a>
          <a class="ms-3" href="#"><i class="fa-regular fa-circle-user"></i></a>
          <div class="ms-3 d-flex align-items-center position-relative" id="search-bar">
            <input class="form-control" type="text" placeholder="Search..." v-model.trim="searchString">
            <a class="position-absolute end-0 pe-4" href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
          </div>
        </nav>
      </header>
      <div class="row pb-5 d-flex justify-content-between">
        <div class="col-4 d-flex align-items-center">
          <div>
            <h1>Complete Your Dreams in JavaS Programming</h1>
            <p>Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.</p>
            <button type="button" class="btn fw-semibold py-2 px-4">
              <i class="fa-solid fa-download"></i> Download Free E-Book
            </button>
          </div>
        </div>
        <div class="col-6 text-end">
          <img id="schooling" src="../assets/img/home-5-hero-image.png" alt="Home schooling">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "HeaderItem",
    props: {
        links: Array,
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/style.scss';
#jumbotron {
  position: relative;
  background-color: $jumbotron;
  &::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 50%;
    bottom: 0;
    background-image: url('../assets/img/jumbo-overlay.svg');
    transform: rotateX(180deg);
  };
  a {
    color: $titles;
  };
  #side-menu {
    top: 180px;
  };
  header {
    height: 100px;
    #logo {
      width: 150px;
    };
    nav {
      height: 100px;
      line-height: 100px;
      ul {
        list-style-type: none;
        height: 100px;
      };
    };
  };
  .col-4 {
    h1 {
      color: $titles;
      font-weight: bold;
      margin-bottom: 1rem;
    }
    p {
      color: $text;
      margin-bottom: 2rem;
    }
    .btn {
      background-color: $jungle_green;
      color: white;
    }
  }
}
</style>