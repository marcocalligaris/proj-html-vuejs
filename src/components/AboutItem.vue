<template>
  <div class="row d-flex justify-content-between" id="about-us">
            <div class="col-6 mb-3">
              <div id="careers-img" class="position-relative text-end">
                <img src="../assets/img/about-us-03-image-01.png" alt="About us">
              </div>
            </div>
            <div class="col-6">
              <div class="generic-title">
                <p>DREAM WITH <strong>MAX COACH</strong></p>
                <h1 class="mb-5"><strong>Construct A </strong><span>Stunning </span><strong>Career Perspective</strong></h1>
              </div>
              <div class="rounded">
                <div>
                  <h6>Multiple Platforms Supported for Teaching & Studying</h6>
                  <a href="#"><i class="fa-solid fa-circle-minus"></i></a>
                </div>
                <div>
                  <p>MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access our knowledge base from any device.</p>
                </div>
              </div>
            </div>
          </div>
</template>

<script>
export default {
name: 'AboutItem',
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/style.scss';
.generic-title {
  h1 {
    color: $mulled_wine;
    span {
      color: $jungle_green;
    }
  };
  p {
    color: $oslo_gray;
  };
};
#careers-img {
  left: -150px;
  background-image: url('../assets/img/underlay-shape-lilla.svg');
  background-repeat: no-repeat;
  background-size: 60%;
  background-position: 80px 120px;
}
</style>