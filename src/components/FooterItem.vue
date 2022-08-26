<template>
  <footer class="position-relative">
      <div class="container">
        <div class="row pb-5">
          <div class="col-6">
            <address class="mb-5">
              <h5 class="fw-bold mb-3">Address</h5>
              <div class="text-secondary fw-semibold">
                <p>382 NE 191st St # 87394 Miami, FL 33179-3899</p>
                <p>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</p>
                <p>support@maxcoach.com</p>
              </div>
            </address>
            <ul class="d-flex">
              <li class="me-4"><a href="#"><i class="fa-brands fa-facebook text-secondary"></i></a></li>
              <li class="me-4"><a href="#"><i class="fa-brands fa-twitter text-secondary"></i></a></li>
              <li class="me-4"><a href="#"><i class="fa-brands fa-instagram text-secondary"></i></a></li>
              <li class="me-4"><a href="#"><i class="fa-brands fa-linkedin text-secondary"></i></a></li>
            </ul>
          </div>
          <div class="col-6 d-flex">
            <div class="col-4">
              <h5 class="fw-bold mb-3">Explore</h5>
              <ul class="text-secondary">
                <li class="mb-3"><a href="#">Start here</a></li>
                <li class="mb-3"><a href="#">Blog</a></li>
                <li class="mb-3"><a href="#">About us</a></li>
              </ul>
            </div>
            <div class="col-4">
              <h5 class="fw-bold mb-3 text-white">EMPTY</h5>
              <ul class="text-secondary">
                <li class="mb-3"><a href="#">Success story</a></li>
                <li class="mb-3"><a href="#">Courses</a></li>
                <li class="mb-3"><a href="#">Contact us</a></li>
              </ul>
            </div>
            <div class="col-4">
              <h5 class="fw-bold mb-3">Information</h5>
              <ul class="text-secondary">
                <li class="mb-3"><a href="#">Membership</a></li>
                <li class="mb-3"><a href="#">Purchase guide</a></li>
                <li class="mb-3"><a href="#">Privacy policy</a></li>
                <li class="mb-3"><a href="#">Terms of services</a></li>
              </ul>
            </div>
          </div>
        </div>
        <p class="text-secondary text-center mb-5"><i class="me-2 fa-regular fa-copyright"></i>2020 Maxcoach. All Rights Reserved</p>
      </div>
      <div><a id="top-arrow" href="#page-start"><i class=" text-white fa-solid fa-arrow-up-long"></i></a></div>
    </footer>
</template>

<script>
export default {
name: 'FooterItem'
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/style.scss';
footer {
  address {
    p {
      font-size: 13px;
    }
  };
  a {
    text-decoration: none;
  };
  #top-arrow {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: $custom_blue;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    right: 20px;
    bottom: 5px;
    &:hover {
    background-color: $mulled_wine;
  }
  }
}
</style>