<template>
  <div class="jumbotron mb-5">
    <div class="rounded-start p-2 d-flex flex-column align-items-center position-absolute end-0" id="side-menu">
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
            <input class="form-control" type="text" placeholder="Search...">
            <a class="position-absolute end-0 pe-4" href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
          </div>
        </nav>
      </header>
      <div class="row pb-5 d-flex justify-content-between">
        <div class="col-4 d-flex align-items-center">
          <div>
            <h1>Complete Your Dreams in JavaS Programming</h1>
            <p>Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.</p>
            <a id="header-btn" class="btn btn-primary fw-semibold py-2 px-4" href="#" role="button"><i class="fa-solid fa-download"></i> Download Free E-Book</a>
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
.jumbotron {
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
    color: $mulled_wine;
  };
  #side-menu {
    top: 180px;
    background-color: $white;
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
  .row {
    .col-4 {
      h1 {
        color: $mulled_wine;
        font-weight: bold;
        margin-bottom: 1rem;
      };
      p {
        color: $oslo_gray;
        margin-bottom: 2rem;
      };
      .btn#header-btn {
        display: inline-block;
        z-index: 10;
        position: relative;
        background-color: $custom_blue;
        color: white;
        &:hover {
          background-color: $mulled_wine !important;
          color: white;
          cursor: pointer;
        }
      };
    };
    #schooling {
      display: inline-block;
      z-index: 10;
      position: relative;
    }
  }
}
</style>