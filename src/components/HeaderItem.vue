<template>
  <div id="jumbotron">
    <!-- Intestazione con menu di navigazione -->
    <div class="container">
      <header class="py-3 d-flex justify-content-between align-items-center">
        <a href="#"><img id="logo" src="../assets/img/dark-logo.png" alt="Max Coach"></a>
        <nav class="d-flex">
          <ul class="d-flex">
            <li v-for="link in links" :key="link.id"
            class="me-5 fw-semibold">
            <a 
            :href="link.url"
            >{{link.text}} <i class="fa-solid fa-angle-down"></i>
            </a>
            </li>
          </ul>

        </nav>
      </header>

    </div>
  </div>
</template>

<script>
export default {
name: 'HeaderItem',
props: {
  links: Array,
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/style.scss';
#jumbotron {
  position: relative;
  overflow: hidden;
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
  header {
    height: 100px;
    line-height: 100px;
    #logo {
      width: 150px;
    }
    ul {
      list-style-type: none;
      a {
        color: $titles;
      }
    }
  }
}
</style>