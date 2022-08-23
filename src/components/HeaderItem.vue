<template>
  <div id="jumbotron">
    
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
}
</style>