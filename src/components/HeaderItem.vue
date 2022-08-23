<template>
  <div id="jumbotron">
    <!-- Intestazione con menu di navigazione -->
    <div class="container">
      <header class="py-3 d-flex justify-content-between align-items-center">
        <a href="#"><img id="logo" src="../assets/img/dark-logo.png" alt="Max Coach"></a>
      </header>

    </div>
  </div>
</template>

<script>
export default {
name: 'HeaderItem',
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
  header #logo {
    width: 150px;
  }
}
</style>